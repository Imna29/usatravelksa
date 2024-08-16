<script setup lang="ts">
import { ref } from 'vue'
import { watchOnce } from '@vueuse/core'
import { Carousel, type CarouselApi, CarouselContent, CarouselItem, CarouselNext, CarouselPrevious } from '@/components/ui/carousel'
import { Card, CardContent } from '@/components/ui/card'
import Autoplay from "embla-carousel-autoplay";

const emblaMainApi = ref<CarouselApi>()
const emblaThumbnailApi = ref<CarouselApi>()
const selectedIndex = ref(0)

const imagePaths = [
  '/gallery_1.jpg',
  '/gallery_2.jpg',
  '/gallery_3.jpg',
  '/gallery_4.jpg',
  '/gallery_5.jpg',
  '/gallery_6.jpg',
  '/gallery_7.jpg',
  '/gallery_8.jpg',
  '/gallery_9.jpg',
  '/gallery_10.jpg'
]

function onSelect() {
  if (!emblaMainApi.value || !emblaThumbnailApi.value)
    return
  selectedIndex.value = emblaMainApi.value.selectedScrollSnap()
  emblaThumbnailApi.value.scrollTo(emblaMainApi.value.selectedScrollSnap())
}

function onThumbClick(index: number) {
  if (!emblaMainApi.value || !emblaThumbnailApi.value)
    return
  emblaMainApi.value.scrollTo(index)
}

watchOnce(emblaMainApi, (emblaMainApi) => {
  if (!emblaMainApi)
    return

  onSelect()
  emblaMainApi.on('select', onSelect)
  emblaMainApi.on('reInit', onSelect)
})
</script>

<template>
  <div class="w-full sm:w-auto">
    <Carousel
        class="relative w-full max-w-2xl"
        @init-api="(val) => emblaMainApi = val"
        :plugins="[Autoplay({
                delay: 2500,
               })]"
        :opts="{
                loop: true,
              }"
    >
      <CarouselContent>
        <CarouselItem v-for="(path, index) in imagePaths" :key="index">
          <div class="p-1">
            <Card>
              <CardContent class="flex aspect-square items-center justify-center p-6">
                <img :src="path" alt="" class="w-full h-full object-cover" />
              </CardContent>
            </Card>
          </div>
        </CarouselItem>
      </CarouselContent>
      <CarouselPrevious />
      <CarouselNext />
    </Carousel>

    <Carousel
        class="relative w-full max-w-2xl"
        @init-api="(val) => emblaThumbnailApi = val"

    >
      <CarouselContent class="flex gap-1 ml-0">
        <CarouselItem v-for="(path, index) in imagePaths" :key="index" class="pl-0 basis-1/4 cursor-pointer" @click="onThumbClick(index)">
          <div class="p-1" :class="index === selectedIndex ? '' : 'opacity-50'">
            <Card>
              <CardContent class="flex aspect-square items-center justify-center p-6">
                <img :src="path" alt="" class="w-full h-full object-cover" />
              </CardContent>
            </Card>
          </div>
        </CarouselItem>
      </CarouselContent>
    </Carousel>
  </div>
</template>
