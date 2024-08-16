<script lang="ts" setup>
import { Quote, Mail, Phone } from "lucide-vue-next";

const faqItems = [
    {
        value: "faq-1",
        title: "What services does UsaTravelKsa offer?",
        content:
            "We offer customized travel packages to Saudi Arabia, including flights, accommodations, guided tours, and 24/7 travel support.",
    },
    {
        value: "faq-2",
        title: "Do you provide visa assistance for Saudi Arabia?",
        content:
            "Yes, we assist with the entire visa application process to make your travel planning as smooth as possible.",
    },
    {
        value: "faq-3",
        title: "What destinations in Saudi Arabia do you cover?",
        content:
            "We primarily cover the holy cities of Mekkah and Madinah, offering tailored experiences in these significant locations.",
    },
    {
        value: "faq-4",
        title: "Can I customize my travel package?",
        content:
            "Absolutely! We offer personalized itineraries tailored to your preferences and interests.",
    },
    {
        value: "faq-5",
        title: "Is it safe to travel to Saudi Arabia?",
        content:
            "Saudi Arabia is generally safe for travelers. We ensure your trip is well-organized and take all necessary precautions to provide a secure experience.",
    },
    {
        value: "faq-6",
        title: "What is the best time to visit Saudi Arabia?",
        content:
            "The best time to visit is during the cooler months, from October to March, when the weather is more comfortable for exploring.",
    },
    {
        value: "faq-7",
        title: "How do I book a trip with UsaTravelKsa?",
        content:
            "You can easily book a trip through our website, or you can contact us directly for personalized assistance.",
    },
    {
        value: "faq-8",
        title: "What payment methods do you accept?",
        content:
            "We accept major credit cards, bank transfers, and online payment platforms.",
    },
    {
        value: "faq-9",
        title: "Do you offer group discounts?",
        content:
            "Yes, we provide special rates for group bookings. Contact us for more details.",
    },
    {
        value: "faq-10",
        title: "What should I pack for my trip to Saudi Arabia?",
        content:
            "We recommend packing modest clothing, comfortable shoes, sunscreen, and any personal necessities. We’ll provide a detailed packing list based on your itinerary.",
    },
];
</script>

<template>
    <div>
        <div class="relative w-full overflow-hidden parallax flex">
            <div class="container flex justify-center z-10 gap-4">
                <div class="my-auto max-w-xl">
                    <div class="text-center text-6xl text-white font-semibold">
                        About Us
                    </div>
                    <div class="text-gray-100 mt-8 text-md">
                        Discover who we are, what drives us, and why
                        UsaTravelKsa is your top choice for Saudi Arabian
                        adventures. Meet our team, explore our values, and see
                        what sets us apart. Learn about our services, read
                        testimonials, and find out why travelers trust us with
                        their journeys.
                    </div>
                </div>
            </div>
            <div
                class="absolute inset-0 w-full h-full bg-primary opacity-60 z-0"
            ></div>
        </div>
        <div class="container pt-8 grid grid-cols-2 gap-12" id="mission">
            <div class="flex">
                <div class="my-auto">
                    <div class="text-4xl font-medium">Our Mission</div>
                    <div class="mt-4 text-gray-700">
                        At UsaTravelKsa, our mission is to create unforgettable
                        travel experiences that connect people with the rich
                        culture, history, and beauty of Saudi Arabia. We are
                        committed to providing personalized, high-quality
                        service that ensures every journey is seamless,
                        enjoyable, and enriching. Our goal is to make your
                        travel dreams a reality by offering exceptional packages
                        that cater to your unique interests and needs, while
                        fostering a deep appreciation for the wonders of Saudi
                        Arabia.
                    </div>
                </div>
            </div>
            <div>
                <NuxtImg
                    src="values.jpg"
                    loading="lazy"
                    class="h-96 rounded-xl mx-auto"
                ></NuxtImg>
            </div>
        </div>
        <div class="bg-primary mt-8 py-8" id="values">
            <div class="container grid grid-cols-2 gap-12">
                <div>
                    <NuxtImg
                        src="mission.jpg"
                        loading="lazy"
                        class="h-96 rounded-xl mx-auto"
                    ></NuxtImg>
                </div>
                <div class="flex">
                    <div class="my-auto">
                        <div class="text-4xl font-medium text-white">
                            Our Values
                        </div>
                        <div class="mt-4 text-gray-300">
                            At UsaTravelKsa, our core values guide every aspect
                            of our business:
                            <ul
                                class="text-gray-300 list-disc list-inside mt-2"
                            >
                                <li class="text-gray-300">
                                    <span class="text-gray-100 font-semibold"
                                        >Exceptional Customer Service:</span
                                    >
                                    We prioritize your experience, ensuring
                                    personalized care and support throughout
                                    your journey.
                                </li>
                                <li class="text-gray-300 mt-2">
                                    <span class="text-gray-100 font-semibold"
                                        >Integrity:</span
                                    >
                                    We operate with honesty and transparency,
                                    building trust through ethical practices.
                                </li>
                                <li class="text-gray-300 mt-2">
                                    <span class="text-gray-100 font-semibold"
                                        >Cultural Respect:</span
                                    >
                                    We honor and celebrate the rich heritage of
                                    Saudi Arabia, creating experiences that are
                                    authentic and respectful.
                                </li>
                                <li class="text-gray-300 mt-2">
                                    <span class="text-gray-100 font-semibold"
                                        >Continuous Improvement:</span
                                    >
                                    We are committed to constantly enhancing our
                                    services to deliver even greater value to
                                    our clients.
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="container mt-8" id="testimonials">
            <div class="lg:text-center">
                <h2
                    class="text-base text-primary font-semibold tracking-wide uppercase"
                >
                    Testimonials
                </h2>
                <p
                    class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl"
                >
                    Traveler Stories
                </p>
            </div>
            <div class="mt-8 grid grid-cols-2 gap-8">
                <div class="p-4 bg-accent rounded-xl">
                    <div><Quote :size="50" /></div>
                    <div class="py-4 text-lg font-medium">
                        Usa TravelKsa Agency' planned the most incredible
                        adventure for our family trip to Riyadh and the desert!
                        Everything was perfectly organized, from the luxurious
                        accommodations to the exciting desert activities. We
                        felt supported throughout the entire trip, and our kids
                        still rave about the camel ride! Thank you, Usa
                        TravelKsa Agency' for making our Saudi Arabian adventure
                        unforgettable.
                    </div>
                    <div>Sarah Jones, San Francisco, CA</div>
                </div>
                <div class="p-4 bg-accent rounded-xl">
                    <div><Quote :size="50" /></div>
                    <div class="py-4 text-lg font-medium">
                        If you're looking for an authentic Saudi Arabian
                        experience that goes beyond the tourist traps, look no
                        further than Usa TravelKsa Agency. Their team curated a
                        personalized itinerary that allowed me to explore the
                        historical treasures of Jeddah and then dive into the
                        crystal-clear waters of the Red Sea. It was the perfect
                        combination of culture and relaxation! Thank you, Usa
                        TravelKsa Agency for exceeding my expectations.
                    </div>
                    <div>Omar Hassan, Dubai, UAE</div>
                </div>
            </div>
        </div>
        <div class="bg-primary mt-8 py-8" id="faqs">
            <div class="container grid grid-cols-2 gap-12">
                <div class="flex my-auto">
                    <NuxtImg
                        src="faq2.jpg"
                        loading="lazy"
                        class="h-96 rounded-xl mx-auto"
                    ></NuxtImg>
                </div>
                <div class="flex flex-col">
                    <div class="text-4xl font-medium text-white">FAQs</div>
                    <div>
                        <Accordion type="single" class="w-full" collapsible>
                            <AccordionItem
                                v-for="item in faqItems"
                                :key="item.value"
                                :value="item.value"
                            >
                                <AccordionTrigger class="text-white">{{
                                    item.title
                                }}</AccordionTrigger>
                                <AccordionContent class="text-white">
                                    {{ item.content }}
                                </AccordionContent>
                            </AccordionItem>
                        </Accordion>
                    </div>
                </div>
            </div>
        </div>
        <div class="mt-8" id="packages">
            <div class="lg:text-center">
                <h2
                    class="text-base text-primary font-semibold tracking-wide uppercase"
                >
                    Packages
                </h2>
                <p
                    class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl"
                >
                    Pricing Plans
                </p>
            </div>
            <SharedPricing class="mt-3"></SharedPricing>
        </div>
        <div class="bg-primary mt-8 py-8" id="contact">
            <div class="container grid gap-12">
                <div class="flex flex-col">
                    <div class="my-auto">
                        <div
                            class="text-4xl font-medium text-white text-center"
                        >
                            Contact Us
                        </div>
                        <div class="flex justify-center">
                            <div class="grid grid-cols-2 mt-8 max-w-2xl flex-1">
                                <div
                                    class="flex flex-col gap-4 justify-center items-center"
                                >
                                    <Mail :size="50" color="white"></Mail>
                                    <div class="text-white">
                                        uastravelksa@gmail.com
                                    </div>
                                </div>
                                <div
                                    class="flex flex-col gap-4 justify-center items-center"
                                >
                                    <Phone :size="50" color="white"></Phone>
                                    <div class="text-white">(267)-123-9874</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.parallax {
    background-image: url("public/about.webp");

    height: 650px;

    background-attachment: fixed;
    background-position: bottom;
    background-repeat: no-repeat;
    background-size: cover;
}
</style>
