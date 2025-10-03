<template>
    <div class="px-5">
        <div class="flex lg:flex-row flex-col-reverse justify-between items-center w-full max-w-[1180px] mx-auto gap-10">
            <div class="lg:max-w-[471px] w-full flex flex-col sm:gap-[50px] gap-[30px]">
                <Heading custom-class="sm:!text-custom-5xl !text-3xl !text-dark-black" text="What Benifit Will You Get">
                </Heading>
                <div class="flex flex-col sm:gap-[30px] gap-5">
                    <div v-for="text in benifits" class="flex items-center gap-5">
                        <Chack />
                        <p class="text-lg leading-100 text-dark-black font-medium">{{ text }}</p>
                    </div>
                </div>
            </div>
            <img src="../assets/images/png/benifit-image.png" alt="benifit image" class="lg:translate-x-[69px] lg:-ml-[69px]">
        </div>
    </div>
</template>
<script setup>
import Chack from '../assets/icons/Chack.vue';
import Heading from './common/Heading.vue';

const benifits = [
    "Free Consulting With Experet Saving Money",
    "Online Banking",
    "Investment Report Every Month",
    "Saving Money For The Future",
    "Online Transection",
];

</script>