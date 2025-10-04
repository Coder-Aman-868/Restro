<template>
    <div class="px-4 sm:px-5 py-16 sm:py-20 lg:py-[130px] relative" id="choose-plan">
        <div class="max-w-[1180px] mx-auto w-full flex flex-col justify-center items-center relative z-50">
            <!-- Header -->
            <Heading
                custom-class="!text-2xl sm:!text-3xl lg:!text-custom-5xl max-w-[280px] sm:max-w-[480px] text-center"
                text="Choose Plan That's Right For You" />
            <Paragraph custom-class="mt-4 sm:mt-6 lg:mt-10 text-center max-w-[320px] sm:max-w-full px-4"
                text="Choose plan that works best for you, feel free to contact us" />

            <!-- Toggle Switch -->
            <div
                class="max-w-full sm:max-w-max w-full bg-white rounded-[10px] p-1.5 sm:p-[7px] flex gap-2 sm:gap-3 shadow-[0_4px_9px_0px_#0000000D] mt-8 sm:mt-10">
                <button @click="togglePlan" :class="ismonthly ? 'bg-light-pink text-white' : 'text-dark-black bg-white'"
                    class="text-sm sm:text-base lg:text-lg font-medium flex-1 sm:flex-initial sm:min-w-[140px] lg:min-w-[160px] leading-[24px] sm:leading-[30px] px-4 sm:px-8 lg:px-[40px] py-2.5 sm:py-3 rounded-[10px] border border-transparent hover:border-light-pink hover:bg-transparent hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">
                    Bill Monthly
                </button>
                <button @click="togglePlan"
                    :class="!ismonthly ? 'bg-light-pink text-white' : 'text-dark-black bg-white'"
                    class="text-sm sm:text-base lg:text-lg font-medium flex-1 sm:flex-initial sm:min-w-[140px] lg:min-w-[160px] leading-[24px] sm:leading-[30px] px-4 sm:px-8 lg:px-[50px] py-2.5 sm:py-3 rounded-[10px] border border-transparent hover:border-light-pink hover:bg-transparent hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">
                    Bill Yearly
                </button>
            </div>

            <!-- Pricing Cards Slider -->
            <div class="w-full mt-12 sm:mt-16 lg:mt-[67px] relative">
                <!-- Slider Container -->
                <div ref="sliderContainer"
                    class="flex gap-3 sm:gap-4 lg:gap-[29px] overflow-x-auto overflow-y-visible scrollbar-hide snap-x snap-mandatory scroll-smooth pb-4 pl-4 pr-4 lg:px-0 lg:justify-center lg:pt-5">
                    <!-- Free Plan Card -->
                    <div
                        class="min-w-[calc(100vw-80px)] sm:min-w-[320px] lg:min-w-[360px] snap-center flex-shrink-0 px-4 sm:px-5 pb-6 sm:pb-[25px] pt-8 sm:pt-10 flex flex-col items-center rounded-[20px] bg-white shadow-[0_4px_9px_0px_#0000000D] hover:shadow-[0_8px_20px_0px_#00000012] transition-all duration-300">
                        <Heading custom-class="!text-2xl sm:!text-custom-3xl !font-semibold" text="Free" />
                        <Paragraph custom-class="my-3 max-w-[200px] text-center text-sm sm:text-base"
                            text="Have a go and test your superpowers" />
                        <div class="relative h-[56px] mb-6 sm:mb-[30px]">
                            <span
                                class="absolute top-0 left-0 text-base sm:text-lg font-medium leading-[30px] text-light-gray">$</span>
                            <h5
                                class="pl-3 sm:pl-4 pt-[26px] text-4xl sm:text-custom-5xl font-semibold leading-[30px] text-dark-black">
                                0
                            </h5>
                        </div>
                        <div class="w-full py-6 sm:py-[26px] px-6 sm:px-[37px] bg-[#F9FAFB] rounded-[10px]">
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">2
                                    Users</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">2
                                    Files</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Public
                                    Share & Comments</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Chat
                                    Support</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-6">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">New
                                    income apps</span>
                            </div>
                            <button
                                class="text-base sm:text-lg font-medium w-full hover:text-white leading-[26px] sm:leading-[30px] hover:bg-light-pink px-6 sm:px-[30px] py-3 sm:py-[17px] rounded-[20px] border border-transparent hover:border-light-pink text-light-pink transition-all duration-300 ease-in-out cursor-pointer shadow-[0px_4px_9px_0px_#0000000D]">
                                Signup for free
                            </button>
                        </div>
                    </div>

                    <!-- Pro Plan Card (Featured) -->
                    <div ref="proCard"
                        class="min-w-[calc(100vw-80px)] overflow-hidden relative sm:min-w-[320px] lg:min-w-[360px] snap-center flex-shrink-0 px-4 sm:px-5 pb-6 sm:pb-[25px] pt-8 sm:pt-10  rounded-[20px] bg-light-pink shadow-[0_4px_9px_0px_#0000000D] hover:shadow-[0_12px_28px_0px_#00000020] transition-all duration-300 lg:scale-105 lg:mx-2">
                        <div class="relative z-50 flex flex-col items-center">
                            <Heading custom-class="!text-2xl sm:!text-custom-3xl !font-semibold !text-white"
                                text="Pro" />
                            <Paragraph custom-class="my-3 max-w-[200px] text-center !text-white text-sm sm:text-base"
                                text="Experiment the power of infinite possibilities" />
                            <div class="relative h-[56px]">
                                <span
                                    class="absolute top-0 left-0 text-base sm:text-lg font-medium leading-[30px] text-white">$</span>
                                <h5
                                    class="pl-3 sm:pl-4 pt-[26px] text-4xl sm:text-custom-5xl font-semibold leading-[30px] text-white">
                                    {{ ismonthly ? "2" : "8" }}
                                </h5>
                            </div>
                            <span
                                class="bg-[#85DAB9] rounded-[10px] py-[5px] px-[11px] text-xs font-semibold leading-[30px] text-white my-4">
                                Save $50 a year
                            </span>
                            <div class="w-full py-6 sm:py-[26px] px-6 sm:px-[37px] bg-white rounded-[10px]">
                                <div class="flex gap-2.5 items-start mb-5">
                                    <Chack
                                        custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                    <span
                                        class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">4
                                        Users</span>
                                </div>
                                <div class="flex gap-2.5 items-start mb-5">
                                    <Chack
                                        custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                    <span
                                        class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">All
                                        apps</span>
                                </div>
                                <div class="flex gap-2.5 items-start mb-5">
                                    <Chack
                                        custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                    <span
                                        class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Unlimited
                                        editable exports</span>
                                </div>
                                <div class="flex gap-2.5 items-start mb-5">
                                    <Chack
                                        custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                    <span
                                        class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Folders
                                        and collaboration</span>
                                </div>
                                <div class="flex gap-2.5 items-start mb-6">
                                    <Chack
                                        custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                    <span
                                        class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">All
                                        incoming apps</span>
                                </div>
                                <button
                                    class="text-base sm:text-lg font-medium w-full text-white leading-[26px] sm:leading-[30px] hover:bg-transparent bg-light-pink px-6 sm:px-[30px] py-3 sm:py-[17px] rounded-[20px] border border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer shadow-[0px_4px_9px_0px_#0000000D]">
                                    Go to pro
                                </button>
                            </div>
                        </div>
                        <div
                            class="bg-[#FF987E] size-[600px] rounded-[9999px] absolute top-[146px] left-1/2 -translate-x-1/2">
                        </div>
                    </div>

                    <!-- Business Plan Card -->
                    <div
                        class="min-w-[calc(100vw-80px)] sm:min-w-[320px] lg:min-w-[360px] snap-center flex-shrink-0 px-4 sm:px-5 pb-6 sm:pb-[25px] pt-8 sm:pt-10 flex flex-col items-center rounded-[20px] bg-white shadow-[0_4px_9px_0px_#0000000D] hover:shadow-[0_8px_20px_0px_#00000012] transition-all duration-300">
                        <Heading custom-class="!text-2xl sm:!text-custom-3xl !font-semibold" text="Business" />
                        <Paragraph custom-class="my-3 max-w-[251px] text-center text-sm sm:text-base"
                            text="Unveil new superpowers and join the Design League" />
                        <div class="relative h-[56px] mb-6 sm:mb-[30px]">
                            <span
                                class="absolute top-0 left-0 text-base sm:text-lg font-medium leading-[30px] text-light-gray">$</span>
                            <h5
                                class="pl-3 sm:pl-4 pt-[26px] text-4xl sm:text-custom-5xl font-semibold leading-[30px] text-dark-black">
                                {{ ismonthly ? "3" : "16" }}
                            </h5>
                        </div>
                        <div class="w-full py-6 sm:py-[26px] px-6 sm:px-[37px] bg-[#F9FAFB] rounded-[10px]">
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">All
                                    the features of pro plan</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Account
                                    success Manager</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Single
                                    Sign-On (SSO)</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-5">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Co-conception
                                    program</span>
                            </div>
                            <div class="flex gap-2.5 items-start mb-6">
                                <Chack
                                    custom-class="!min-w-[22px] !min-h-[22px] sm:!min-w-[26px] sm:!min-h-[26px] w-[22px] h-[22px] sm:w-[26px] sm:h-[26px] mt-0.5" />
                                <span
                                    class="text-base sm:text-lg font-medium leading-[26px] sm:leading-[30px] text-dark-black">Collaboration-Soon</span>
                            </div>
                            <button
                                class="text-base sm:text-lg font-medium w-full hover:text-white leading-[26px] sm:leading-[30px] hover:bg-light-pink px-6 sm:px-[30px] py-3 sm:py-[17px] rounded-[20px] border border-transparent hover:border-light-pink text-light-pink transition-all duration-300 ease-in-out cursor-pointer shadow-[0px_4px_9px_0px_#0000000D]">
                                Go to Business
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Navigation Arrows (Desktop Only) -->
                <button @click="scrollLeft"
                    class="hidden lg:flex absolute left-0 top-1/2 -translate-y-1/2 -translate-x-4 z-10 items-center justify-center w-12 h-12 rounded-full bg-white shadow-[0_4px_12px_0px_#00000015] hover:shadow-[0_6px_20px_0px_#00000025] hover:bg-light-pink hover:text-white transition-all duration-300 cursor-pointer group">
                    <svg class="w-6 h-6 text-light-pink group-hover:text-white transition-colors" fill="none"
                        stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                    </svg>
                </button>
                <button @click="scrollRight"
                    class="hidden lg:flex absolute right-0 top-1/2 -translate-y-1/2 translate-x-4 z-10 items-center justify-center w-12 h-12 rounded-full bg-white shadow-[0_4px_12px_0px_#00000015] hover:shadow-[0_6px_20px_0px_#00000025] hover:bg-light-pink hover:text-white transition-all duration-300 cursor-pointer group">
                    <svg class="w-6 h-6 text-light-pink group-hover:text-white transition-colors" fill="none"
                        stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                    </svg>
                </button>

                <!-- Scroll Indicators (Mobile) -->
                <div class="flex lg:hidden justify-center gap-2 mt-6">
                    <span v-for="i in 3" :key="i"
                        :class="currentSlide === i - 1 ? 'bg-light-pink w-8' : 'bg-gray-300 w-2'"
                        class="h-2 rounded-full transition-all duration-300"></span>
                </div>
            </div>
        </div>

        <!-- Background Blur Effect -->
        <div
            class="bg-light-pink w-[300px] h-[300px] sm:w-[450px] sm:h-[450px] lg:w-[634px] lg:h-[634px] rounded-full blur-[250px] sm:blur-[350px] lg:blur-[500px] absolute top-0 -right-[150px] sm:-right-[225px] lg:-right-[317px] opacity-70 pointer-events-none">
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted, nextTick } from 'vue';
import Heading from './common/Heading.vue';
import Paragraph from './common/Paragraph.vue';
import Chack from '../assets/icons/Chack.vue';

const ismonthly = ref(true);
const sliderContainer = ref(null);
const proCard = ref(null);
const currentSlide = ref(1);

const togglePlan = () => {
    ismonthly.value = !ismonthly.value;
};

const scrollLeft = () => {
    if (sliderContainer.value) {
        sliderContainer.value.scrollBy({
            left: -400,
            behavior: 'smooth'
        });
    }
};

const scrollRight = () => {
    if (sliderContainer.value) {
        sliderContainer.value.scrollBy({
            left: 400,
            behavior: 'smooth'
        });
    }
};

const updateCurrentSlide = () => {
    if (sliderContainer.value) {
        const scrollLeft = sliderContainer.value.scrollLeft;
        const cardWidth = sliderContainer.value.offsetWidth;
        currentSlide.value = Math.round(scrollLeft / cardWidth);
    }
};

const scrollToProCard = () => {
    nextTick(() => {
        if (proCard.value) {
            proCard.value.scrollIntoView({
                behavior: 'smooth',
                block: 'nearest',
                inline: 'center'
            });
        }
    });
};

onMounted(() => {
    if (sliderContainer.value) {
        sliderContainer.value.addEventListener('scroll', updateCurrentSlide);
    }

    setTimeout(scrollToProCard, 100);
});

onUnmounted(() => {
    if (sliderContainer.value) {
        sliderContainer.value.removeEventListener('scroll', updateCurrentSlide);
    }
});
</script>

<style scoped>
.scrollbar-hide::-webkit-scrollbar {
    display: none;
}

.scrollbar-hide {
    -ms-overflow-style: none;
    scrollbar-width: none;
}
</style>