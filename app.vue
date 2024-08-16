<script lang="ts" setup>
useHead({
    title: "UsaTravelKsa",
    meta: [
        {
            name: "description",
            content:
                "Discover unforgettable travel experiences with UsaTravelKsa, your trusted partner for personalized journeys to the holy cities of Mekkah and Madinah. We specialize in custom travel packages, including visa assistance, accommodations, guided tours, and more. Whether you're planning a pilgrimage or exploring Saudi Arabia's rich cultural heritage, our dedicated team ensures a seamless, secure, and enriching travel experience. Book your next adventure with UsaTravelKsa and embark on a journey of a lifetime.",
        },
    ],
});
</script>

<template>
    <div class="">
        <SharedHeaderBanner></SharedHeaderBanner>
        <SharedHeader class="py-2 static top-0"></SharedHeader>
        <NuxtPage />
    </div>
</template>

<style>
.page-enter-active,
.page-leave-active {
    transition: all 0.2s;
}
.page-enter-from,
.page-leave-to {
    opacity: 0;
    filter: blur(1rem);
}

* {
    font-family: "Roboto Serif", serif;
    color: hsl(var(--primary));
}

html {
    scroll-behavior: smooth;
}
</style>
