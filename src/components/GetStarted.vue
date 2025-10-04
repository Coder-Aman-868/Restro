<template>
    <div class="px-5 bg-dark-nevy-blue md:pt-[130px] md:pb-[170px] sm:py-20 py-15" id="contact">
        <div class="flex max-w-[1180px] mx-auto w-full justify-between items-stretch gap-x-5 gap-y-15 lg:flex-row flex-col">
            <div class="lg:max-w-[466px] w-full">
                <Heading custom-class="sm:!text-custom-5xl !text-3xl !text-white !leading-125 !text-semibold"
                    text="People are Saying About DoWhith" />
                <Paragraph custom-class="mt-5 sm:mb-[42px] mb-7"
                    text="Everything you need to accept to payment and grow your money of manage anywhere on planet" />
                <Sami />
                <Paragraph custom-class="sm:my-[40px] my-7"
                    text="Everything you need to accept to payment and grow your money of manage anywhere on planet" />
                <Paragraph custom-class="sm:mb-[40px] mb-7" text="_ Aria Zinanrio" />
                <div class="flex gap-5 items-center flex-wrap flex-row">
                    <img v-for="images in getStartedData" :src='images' :key="images" alt="images">
                </div>
            </div>
            <div class="lg:max-w-[612px] w-full bg-nevy-blue sm:py-[53px] sm:px-[86px] py-10 px-10 rounded-[20px]">
                <h3 class="text-custom-3xl font-medium text-white leading-100 text-center sm:mb-[106px] mb-10">Get Started</h3>
                <form class="flex flex-col gap-5">
                    <label class="text-lg font-medium leading-100 text-white" for="email">Email</label>
                    <input id="email" type="text" placeholder="Enter your email"
                        class="rounded-[10px] bg-white text-sm font-medium leading-100 py-[17px] px-5 outline-none placeholder:text-light-gray" />
                    <label class="text-lg font-medium leading-100 text-white" for="message">Message</label>
                    <textarea id="message" type="text" placeholder="What are you say ?"
                        class="rounded-[10px] bg-white text-sm font-medium leading-100 py-[17px] px-5 outline-none placeholder:text-light-gray h-20" />
                        <button class="w-full bg-light-pink text-white border border-transparent text-base font-semibold leading-100 py-5 rounded-[10px] hover:bg-transparent hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer text-nowrap">Request Demo</button>
                </form>
                <div class="ml-auto text-end mt-2.5 max-w-max text-white"><span class="opacity-50">or </span> Start Free Trial</div>
            </div>
        </div>
    </div>
</template>
<script setup>
import Sami from '../assets/icons/Sami.vue';
import Heading from './common/Heading.vue';
import Paragraph from './common/Paragraph.vue';
import getStartedImg1 from '../assets/images/png/get-started-img-1.png';
import getStartedImg2 from '../assets/images/png/get-started-img-2.png';
import getStartedImg3 from '../assets/images/png/get-started-img-3.png';
import getStartedImg4 from '../assets/images/png/get-started-img-4.png';
import getStartedImg5 from '../assets/images/png/get-started-img-5.png';

const getStartedData = [
    getStartedImg1,
    getStartedImg2,
    getStartedImg3,
    getStartedImg4,
    getStartedImg5,
]

</script>