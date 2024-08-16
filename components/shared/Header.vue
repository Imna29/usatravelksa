<script lang="ts" setup>
import { navigationMenuTriggerStyle } from "@/components/ui/navigation-menu";
import { Phone, MapPin } from "lucide-vue-next";

const components: { title: string; href: string; description: string }[] = [
    {
        title: "Our Mission",
        href: "/about#mission",
        description: "Learn about the journey and passion behind UsaTravelKsa.",
    },
    {
        title: "Our Values",
        href: "/about#values",
        description: "Discover the principles that guide everything we do.",
    },
    {
        title: "Testimonials",
        href: "/about#testimonials",
        description:
            "See what our customers have to say about their experiences.",
    },
    {
        title: "Frequently Asked Questions",
        href: "/about#faqs",
        description: "Get answers to common questions about traveling with us.",
    },
    {
        title: "Contact Us",
        href: "/about#contact",
        description: "Reach out to us for any inquiries or booking assistance.",
    },
    {
        title: "Packages",
        href: "/about#packages",
        description:
            "Take a look at our custom crafted packages tailored just for you.",
    },
];
</script>

<template>
    <div class="container flex">
        <NuxtLink to="/"><img src="/public/logo.svg" width="75" /></NuxtLink>
        <div class="my-auto text-3xl ml-2 name">
            <span><NuxtLink to="/">UsaTravelKsa</NuxtLink></span>
        </div>
        <NavigationMenu class="mx-auto z-30">
            <NavigationMenuList>
                <NavigationMenuItem>
                    <NuxtLink to="/">
                        <NavigationMenuTrigger
                            :class="navigationMenuTriggerStyle()"
                            >Home</NavigationMenuTrigger
                        >
                    </NuxtLink>
                    <NavigationMenuContent>
                        <ul
                            class="grid gap-3 p-6 md:w-[400px] lg:w-[500px] lg:grid-cols-[minmax(0,.75fr)_minmax(0,1fr)]"
                        >
                            <li class="row-span-3">
                                <NavigationMenuLink as-child>
                                    <NuxtLink
                                        class="flex h-full w-full select-none flex-col justify-end rounded-md bg-muted p-6 no-underline outline-none focus:shadow-md"
                                        to="/"
                                    >
                                        <img
                                            src="/public/menu_home_1.jpg"
                                            class="rounded-md"
                                        />
                                        <div
                                            class="mb-2 mt-4 text-sm font-medium"
                                        >
                                            <MapPin class="inline mr-1" />Taif,
                                            Makkah Province, Saudi Arabia
                                        </div>
                                        <p
                                            class="text-sm leading-tight text-muted-foreground"
                                        >
                                            View of an Alley between Buildings
                                            in Taif, Makkah Province in Saudi
                                            Arabia
                                        </p>
                                    </NuxtLink>
                                </NavigationMenuLink>
                            </li>

                            <li>
                                <NavigationMenuLink as-child>
                                    <NuxtLink
                                        to="/"
                                        class="block select-none space-y-1 rounded-md p-3 leading-none no-underline outline-none transition-colors hover:bg-accent hover:text-accent-foreground focus:bg-accent focus:text-accent-foreground"
                                    >
                                        <div
                                            class="text-sm font-medium leading-none"
                                        >
                                            Home
                                        </div>
                                        <p
                                            class="line-clamp-2 text-sm leading-snug text-muted-foreground"
                                        >
                                            Explore our website.
                                        </p>
                                    </NuxtLink>
                                </NavigationMenuLink>
                            </li>
                            <li>
                                <NavigationMenuLink as-child>
                                    <NuxtLink
                                        to="/#packages"
                                        class="block select-none space-y-1 rounded-md p-3 leading-none no-underline outline-none transition-colors hover:bg-accent hover:text-accent-foreground focus:bg-accent focus:text-accent-foreground"
                                    >
                                        <div
                                            class="text-sm font-medium leading-none"
                                        >
                                            Packages
                                        </div>
                                        ``
                                        <p
                                            class="line-clamp-3 text-sm leading-snug text-muted-foreground"
                                        >
                                            Take a look at our custom crafted
                                            packages tailored just for you.
                                        </p>
                                    </NuxtLink>
                                </NavigationMenuLink>
                            </li>
                            <li>
                                <NavigationMenuLink as-child>
                                    <NuxtLink
                                        to="/#gallery"
                                        class="block select-none space-y-1 rounded-md p-3 leading-none no-underline outline-none transition-colors hover:bg-accent hover:text-accent-foreground focus:bg-accent focus:text-accent-foreground"
                                    >
                                        <div
                                            class="text-sm font-medium leading-none"
                                        >
                                            Gallery
                                        </div>
                                        <p
                                            class="line-clamp-3 text-sm leading-snug text-muted-foreground"
                                        >
                                            Explore pictures of the magical
                                            place that is The Kingdom Of Saudi
                                            Arabia
                                        </p>
                                    </NuxtLink>
                                </NavigationMenuLink>
                            </li>
                        </ul>
                    </NavigationMenuContent>
                </NavigationMenuItem>
                <NavigationMenuItem>
                    <NuxtLink to="/about">
                        <NavigationMenuTrigger
                            :class="navigationMenuTriggerStyle()"
                            >About</NavigationMenuTrigger
                        >
                    </NuxtLink>
                    <NavigationMenuContent>
                        <ul
                            class="grid w-[400px] gap-3 p-4 md:w-[500px] md:grid-cols-2 lg:w-[600px]"
                        >
                            <li
                                v-for="component in components"
                                :key="component.title"
                            >
                                <NavigationMenuLink as-child>
                                    <NuxtLink
                                        :to="component.href"
                                        class="block select-none space-y-1 rounded-md p-3 leading-none no-underline outline-none transition-colors hover:bg-accent hover:text-accent-foreground focus:bg-accent focus:text-accent-foreground"
                                    >
                                        <div
                                            class="text-sm font-medium leading-none"
                                        >
                                            {{ component.title }}
                                        </div>
                                        <p
                                            class="line-clamp-2 text-sm leading-snug text-muted-foreground"
                                        >
                                            {{ component.description }}
                                        </p>
                                    </NuxtLink>
                                </NavigationMenuLink>
                            </li>
                        </ul>
                    </NavigationMenuContent>
                </NavigationMenuItem>
                <NavigationMenuItem>
                    <NuxtLink to="/#packages">
                        <NavigationMenuLink
                            :class="navigationMenuTriggerStyle()"
                        >
                            Packages
                        </NavigationMenuLink></NuxtLink
                    >
                </NavigationMenuItem>
                <NavigationMenuItem>
                    <NuxtLink to="/about#contact">
                        <NavigationMenuLink
                            :class="navigationMenuTriggerStyle()"
                        >
                            Contact
                        </NavigationMenuLink>
                    </NuxtLink>
                </NavigationMenuItem>
            </NavigationMenuList>
        </NavigationMenu>
        <div class="my-auto p-2 bg-muted rounded-2xl">
            <Phone class="text-primary" />
        </div>
        <div class="my-auto ml-2">
            <div>Customer Care</div>
            <div>267-123-9874</div>
        </div>
    </div>
</template>

<style>
.name {
    font-family: "Urbanist", sans-serif !important;
    font-optical-sizing: auto;
    font-weight: 500;
    font-style: normal;
}
</style>
