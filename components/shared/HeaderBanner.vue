<script setup lang="ts">
import { Facebook, Instagram } from "lucide-vue-next";
</script>

<template>
    <div class="w-full bg-primary py-2">
        <div class="container flex">
            <div class="text-white">
                Limited Time Deals!
                <NuxtLink to="/#packages">
                    <span class="underline text-white">Explore now</span>
                </NuxtLink>
            </div>
            <div class="flex ml-auto text-white">
                <Facebook color="white" class="mr-2"></Facebook>
                Facebook |
                <Instagram color="white" class="ml-2 mr-2"></Instagram>
                Instagram
            </div>
        </div>
    </div>
</template>

<style scoped></style>
