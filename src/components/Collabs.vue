<template>
    <div class="px-5 py-[130px]">
        <div class="max-w-[1180px] mx-auto w-full flex-col flex justify-center items-center">
            <Heading custom-class="sm:!text-[40px] !text-3xl !text-dark-black" text="More than 25,000 teams use Collabs">
            </Heading>
            <Vue3Marquee class="mt-[61px] text-" :pauseOnHover="true" >
                <img class="ml-10" src="../assets/images/png/descript.png" />
                <img class="ml-10" src="../assets/images/png/grammarly.png" />
                <img class="ml-10" src="../assets/images/png/intercom.png" />
                <img class="ml-10" src="../assets/images/png/notion.png" />
                <img class="ml-10" src="../assets/images/png/unsplash.png" />
                <img class="ml-10" src="../assets/images/png/intercom.png" />
            </Vue3Marquee>
        </div>
    </div>
</template>
<script setup>
import { Vue3Marquee } from 'vue3-marquee';
import Heading from './common/Heading.vue';

</script>