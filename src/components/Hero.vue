<template>
    <div class="px-5" id="home">
        <div class="max-w-[1180px] mx-auto w-full flex justify-center items-center lg:flex-row flex-col-reverse">
            <div class="w-full lg:max-w-[555px]">
                <Heading
                    custom-class="xl:!text-[80px] md:!text-[70px] !text-custom-5xl md:!leading-[90px] leading-100 !text-dark-black sm:mb-[30px] mb-4"
                    text="We’re here to Increase your Productivity">
                </Heading>
                <div class="sm:flex hidden">
                    <Line />
                </div>
                <Paragraph class="!text-black sm:my-[50px] my-7"
                    text="Let's make your work more organize and easily using the Taskio Dashboard with many of the latest featuresin managing work every day." />
                <div class=" flex sm:gap-10 gap-5 items-center sm:flex-row flex-col">
                    <button
                        class="text-lg font-medium sm:max-w-max w-full text-white leading-100 bg-light-pink px-[30px] py-5 rounded-[30px] border border-transparent hover:border-light-pink hover:bg-transparent hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">Try
                        free trial</button>
                    <button
                        class="flex justify-center items-center gap-1 text-lg font-medium sm:max-w-max w-full text-dark-black leading-100 transition-all duration-300 ease-in-out cursor-pointer">
                        <PlayPause /> View Demo
                    </button>
                </div>
            </div>
            <img class="xl:w-[653px] w-[500px] object-contain translate-y-[-40px] -mb-7"
                src="../assets/images/png/hero-image.png" alt="hero image" />
        </div>
    </div>
</template>
<script setup>
import Line from '../assets/icons/Line.vue';
import PlayPause from '../assets/icons/PlayPause.vue';
import Heading from './common/Heading.vue';
import Paragraph from './common/Paragraph.vue';

</script>