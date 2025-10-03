<template>
    <div class="px-5 py-15 bg-clay-gray">
        <div class="max-w-[1180px] mx-auto w-full flex justify-center items-center gap-7 max-[1200px]:flex-col">
            <div class="flex flex-col min-[1200px]:max-w-[644px] w-full">
                <Heading custom-class="sm:!text-custom-5xl !text-3xl !text-dark-black"
                    text="How we support our pratner all over the world"></Heading>
                <Paragraph customClass="mt-[30px] min-[1200px]:mb-[73px] mb-[30px]"
                    text="SaaS become a common delivery model for many business application, including office software, messaging software, payroll processing software, DBMS software, management software" />
                <div class="flex sm:gap-20 sm:justify-start justify-between">
                    <div class="flex flex-col gap-[18px]">
                        <FiveStar />
                        <span class="text-lg leading-100"><b>4.9</b> / 5 rating</span>
                        <p class="text-lg leading-100 text-light-gray font-bold">databricks</p>
                    </div>
                    <div class="flex flex-col gap-[18px]">
                        <FourStar />
                        <span class="text-lg leading-100"><b>4.8</b> / 5 rating</span>
                        <p class="text-lg leading-100 text-light-gray font-bold">Chainalysis</p>
                    </div>
                </div>
            </div>
            <div class="flex flex-col gap-[30px] max-[1200px]:w-full">
                <div v-for="item in supportData" :key="item.heading" class="flex sm:flex-row flex-col gap-[21px] items-start">
                    <div class="p-[18.5px] shadow-[0px_4px_9px_0px_#0000000D] bg-white">
                        <component :is="item.icon" />
                    </div>
                    <div class="flex flex-col ">
                        <Heading custom-class="!text-custom-3xl !text-dark-black" :text="item.heading"></Heading>
                        <Paragraph custom-class="!mt-2.5" :text="item.paragraph"></Paragraph>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import Analytics from '../assets/icons/Analytics.vue';
import Engagement from '../assets/icons/Engagement.vue';
import FiveStar from '../assets/icons/FiveStar.vue';
import FourStar from '../assets/icons/FourStar.vue';
import Publishing from '../assets/icons/Publishing.vue';
import Heading from './common/Heading.vue';
import Paragraph from './common/Paragraph.vue';

const supportData = [
    {
        icon: Publishing,
        heading: "Publishing",
        paragraph: "Plan, collaborate, and publishing your contetn that drivees meaningful engagement and growth for your barnd"
    },
    {
        icon: Analytics,
        heading: "Analytics",
        paragraph: "Analyze your performance and create goegeous report"
    },
    {
        icon: Engagement,
        heading: "Engagement",
        paragraph: "Quiuckly navigate you anda engage with your adience"
    },
]

</script>