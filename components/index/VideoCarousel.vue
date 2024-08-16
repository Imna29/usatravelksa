<script setup lang="ts">
import {ref} from 'vue'
import {watchOnce} from '@vueuse/core'
import type {CarouselApi} from '@/components/ui/carousel'
import {Carousel, CarouselContent, CarouselItem, CarouselNext, CarouselPrevious} from '@/components/ui/carousel'
import {Card, CardContent} from '@/components/ui/card'
import Autoplay from 'embla-carousel-autoplay'

const api = ref<CarouselApi>()
const totalCount = ref(0)
const current = ref(0)

const videos = [
  'makkah_1.mp4',
  'makkah_2.mp4',
  'makkah_3.mp4',
  'madinah_1.mp4',
  'madinah_2.mp4'
]

function setApi(val: CarouselApi) {
  api.value = val
}

watchOnce(api, (api) => {
  if (!api) return
  totalCount.value = api.scrollSnapList().length
  current.value = api.selectedScrollSnap() + 1
  api.on('select', () => {
    current.value = api.selectedScrollSnap() + 1
  })
})
</script>

<template>
  <div class="w-full sm:w-auto">
    <Carousel class="relative w-[90%] ml-auto" @init-api="setApi"
              :plugins="[Autoplay({
                delay: 5000,
               })]"
              :opts="{
                loop: true,
              }"
    >
      <CarouselContent>
        <CarouselItem v-for="(video, index) in videos" :key="index">
          <div class="p-1">
            <Card>
              <CardContent class="flex aspect-square items-center justify-center p-6">
                <video
                    :src="video"
                    autoplay
                    controls
                    muted
                    loop
                    class="w-full h-full object-cover"
                >
                  Your browser does not support the video tag.
                </video>
              </CardContent>
            </Card>
          </div>
        </CarouselItem>
      </CarouselContent>
      <CarouselPrevious/>
      <CarouselNext/>
    </Carousel>
    <div class="py-2 text-center text-sm text-muted-foreground">
      Video {{ current }} of {{ totalCount }}
    </div>
  </div>
</template>