<template>
    <div class="px-5 bg-dark-nevy-blue">
        <div class="max-w-[1180px] mx-auto w-full flex justify-between lg:items-center gap-5 gap-y-15 lg:flex-row flex-col">
            <div class="flex flex-col max-w-[410px] w-full">
                <h2 class="text-light-pink sm:text-custom-5xl text-4xl font-semibold leading-[30px]">Restro</h2>
                <Paragraph text="Get started noew try our product" custom-class="my-[30px]" />
                <form class="flex relative">
                    <input required type="email" placeholder="Enter your email here"
                        class="border-2 border-light-gray rounded-[70px] py-[15px] px-5 w-full outline-none placeholder:text-light-gray text-lg font-medium leading-[30px]" />
                    <button
                        class="size-[50px] rounded-[999px] bg-light-pink absolute right-[7px] top-[7px] border border-transparent hover:bg-transparent hover:border-light-pink group transition-all duration-300 ease-in-out flex justify-center items-center">
                        <RightArrow />
                    </button>
                </form>
            </div>
            <div class="max-w-[587px] w-full flex justify-between gap-5 flex-wrap flex-row gap-y-10">
                <ul v-for="link in links" :key="link.title" class="flex flex-col gap-5">
                    <li>
                        <Paragraph custom-class="!text-white" :text="link.title" />
                    </li>
                    <li v-for="link in link.links" :key="link.name"
                        class="text-light-gray hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">
                        <a class="hover:text-light-pink transition-all duration-300 ease-in-out after:absolute relative after:-bottom-1 after:left-1/2 after:-translate-x-1/2 after:w-0 after:h-[3px] after:rounded-2xl after:bg-light-pink hover:after:w-full after:transition-all after:duration-300 after:ease-in-out" :href="link.link">{{ link.name }}</a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="max-w-[1180px] mx-auto w-full flex justify-between items-center pt-[59px] pb-10 flex-wrap gap-5 md:flex-row flex-col">
            <Paragraph custom-class="!text-white" text="© 2025 Biccas Inc. Copyright and rights reserved" />
            <div class="flex gap-2.5 items-center">
                <Paragraph custom-class="!text-white cursor-pointer" text="Terms and Condtions" />
                <Dot />
                <Paragraph custom-class="!text-white cursor-pointer" text="Privacy Policy" />
            </div>
        </div>
    </div>
</template>
<script setup>
import Paragraph from './common/Paragraph.vue';
import RightArrow from '../assets/icons/RightArrow.vue';
import Dot from '../assets/icons/Dot.vue';

const links = [
    {
        title: "Support",
        links: [
            {
                name: "Help centre",
                path: "help-centre"
            },
            {
                name: "Account information",
                path: "account-information"
            },
            {
                name: "About",
                path: "about"
            },
            {
                name: "Contact us",
                path: "contect-us"
            },
        ]
    },
    {
        title: "Help and Solution",
        links: [
            {
                name: "Talk to support",
                path: "talk-to-support"
            },
            {
                name: "Support docs",
                path: "support-docs"
            },
            {
                name: "System status",
                path: "system-status"
            },
            {
                name: "Covid responde",
                path: "covid-responde"
            },
        ]
    },
    {
        title: "Product",
        links: [
            {
                name: "Update",
                path: "update"
            },
            {
                name: "Security",
                path: "security"
            },
            {
                name: "Beta test",
                path: "beta-test"
            },
            {
                name: "Pricing product",
                path: "pricing-product"
            },
        ]
    },
]

</script>