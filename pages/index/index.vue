<script lang="ts" setup>
import {Button} from "~/components/ui/button";
import {ArrowRight} from 'lucide-vue-next';

</script>

<template>
  <div>
    <div class="relative w-full overflow-hidden parallax flex">
      <div class="container flex flex-col justify-center z-10 gap-4">
        <div class="bg-white w-fit p-2 bg-opacity-15 font-medium rounded-md text-white">
          Feed the Experience
        </div>
        <div class="text-6xl w-1/2 text-white font-semibold">
          Embark on a Memorable Journey to Saudi Arabia with Us
        </div>
        <div>
          <Button class="text-lg">
            Book Now
            <ArrowRight class="w-5 h-5 ml-2" color="white"/>
          </Button>
        </div>
      </div>
      <div class="absolute inset-0 w-full h-full bg-primary opacity-50 z-0">

      </div>
    </div>
    <div class="container flex gap-2 pt-8">
      <div class="flex-1 bg-accent p-4 rounded-lg">
        <div class="mt-3 uppercase font-semibold text-sm text-blue-950">
          About Us
        </div>
        <div class="text-4xl mt-3 leading-relaxed">
          Crafting Unforgettable Saudi Adventures Since 2023
        </div>
        <div class="mt-3 font-medium leading-relaxed">
          Welcome to UsaTravelKsa! We’re here to make your dream trip to Saudi Arabia come true. Our passion is creating
          amazing travel experiences that you’ll remember forever. Whether you want to explore rich history,
          breathtaking landscapes, or vibrant cities, we’ve got the perfect package for you.
        </div>
        <div class="mt-3 font-light leading-relaxed">
          Our friendly and knowledgeable team is dedicated to making your journey smooth and enjoyable. We handle all
          the details so you can focus on having a great time. At UsaTravelKsa, we’re about creating unforgettable
          memories. Join us and let’s explore the wonders of Saudi Arabia together!
        </div>
        <div class="mt-8 flex">
          <div class="flex-1 flex items-center">
            <Button class="text-lg">
              Our Profile
              <ArrowRight class="w-5 h-5 ml-2" color="white"/>
            </Button>
          </div>
          <div class="flex-1 flex gap-4">
            <div>
              <img src="/public/aqlan.webp" class="h-20 rounded-3xl"></img>
            </div>
            <div>
              <div>
                Director
              </div>
              <div class="text-2xl font-bold mt-2">
                Mohammed Aqlan
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="flex-1">
        <IndexVideoCarousel class="w-full h-full"></IndexVideoCarousel>
      </div>
    </div>
    <div class="mt-8" id="packages">
      <div class="lg:text-center">
        <h2 class="text-base text-primary font-semibold tracking-wide uppercase">Packages</h2>
        <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">Pricing Plans</p>
      </div>
      <SharedPricing class="mt-3"></SharedPricing>
    </div>
    <div class="mt-8 flex flex-col gap-4" id="gallery">
      <div class="lg:text-center">
        <h2 class="text-base text-primary font-semibold tracking-wide uppercase">Gallery</h2>
        <p class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">Explore Saudi
          Arabia</p>
      </div>
      <IndexPictureCarousel class="mx-auto pb-4"></IndexPictureCarousel>
    </div>
  </div>
</template>

<style scoped>
.parallax {
  background-image: url("public/main_cover.jpg");

  height: 650px;

  background-attachment: fixed;
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
