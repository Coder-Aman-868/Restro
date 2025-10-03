<template>
    <div class="px-5 md:py-[130px] sm:py-20 py-[60px] relative">
        <div
            class="max-w-[1180px] mx-auto w-full flex justify-center items-center flex-col md:gap-[74px] sm:gap-[50px] gap-10 relative z-50">
            <div class="flex justify-between items-center gap-5 w-full flex-row flex-wrap">
                <Heading custom-class="sm:!text-custom-5xl !text-3xl !text-dark-black lg:max-w-[331px]"
                    text="Our Features you cab get">
                </Heading>
                <Paragraph customClass="text-light-gray max-w-[461px]"
                    text="We offer a variety of interesting features that you can help increase yor productivity at work and manage your projrct esaly" />
                <button
                    class="text-lg font-medium sm:max-w-max w-full text-white leading-100 bg-light-pink px-[30px] py-5 rounded-[30px] border border-transparent hover:border-light-pink hover:bg-transparent hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">
                    Get Started</button>
            </div>
            <div
                class="grid md:grid-cols-3 sm:grid-cols-2 grid-cols-1 justify-center items-center lg:gap-11 gap-y-11 gap-6 w-full">
                <div v-for="feature in features" :key="feature.heading"
                    class="flex flex-col w-full justify-between items-stretch text-center">
                    <img class="max-sm:!w-[200px] mx-auto" :src="feature.image" alt="feature image" />
                    <Heading custom-class="lg:!text-custom-3xl text-2xl !text-dark-black sm:mt-[30px] sm:mb-5 my-2.5"
                        :text="feature.heading">
                    </Heading>
                    <Paragraph customClass="text-light-gray" :text="feature.paragraph"></Paragraph>
                </div>
            </div>
        </div>
        <div class="bg-light-pink size-[634px] rounded-[9999px] blur-[1000px] absolute top-[441px] -left-[194px]"></div>
    </div>
</template>
<script setup>
import Heading from './common/Heading.vue';
import Paragraph from './common/Paragraph.vue';
import featuresImage1 from '../assets/images/png/collboration-teams.png';
import featuresImage2 from '../assets/images/png/cloud-storage.png';
import featuresImage3 from '../assets/images/png/daily-analytics.png';

const features = [
    {
        image: featuresImage1,
        heading: "Collboration Teams",
        paragraph: "Here you can handle projects together with team virtually"
    },
    {
        image: featuresImage2,
        heading: "Cloud Storages",
        paragraph: "No nedd to worry about storage because we provide storage up to 2 TB"
    },
    {
        image: featuresImage3,
        heading: "Daily Analytics",
        paragraph: "We always provide useful informatin to make it easier for you every day"
    },
];

</script>