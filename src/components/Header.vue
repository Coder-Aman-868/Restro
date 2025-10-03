<template>
    <div class="px-5 sm:py-10 py-5">
        <div class="max-w-[1180px] mx-auto w-full flex justify-between items-center">
            <h2 class="text-light-pink sm:text-custom-5xl text-4xl font-semibold leading-[30px]">Restro</h2>
            <div class="flex lg:justify-between justify-end items-center gap-10 max-w-[681px] w-full">
                <ul :class="[
                    'flex gap-10 justify-center',
                    'max-lg:flex-col max-lg:items-center max-lg:h-screen max-lg:w-full max-lg:bg-white z-[99]',
                    open ? 'max-lg:right-0' : 'max-lg:-right-full',
                    'max-lg:fixed max-lg:top-0 max-lg:gap-5 duration-300 ease-in-out'
                ]">
                    <li v-for="link in links" class="text-base text-light-gray font-medium leading-100" :key="index">
                        <a @click="toggleByNavLinks"
                            class="hover:text-light-pink transition-all duration-300 ease-in-out after:absolute relative after:-bottom-1 after:left-1/2 after:-translate-x-1/2 after:w-0 after:h-1 after:rounded-2xl after:bg-light-pink hover:after:w-full after:transition-all after:duration-300 after:ease-in-out"
                            :href="link.path">{{ link.name }}</a>
                    </li>
                    <li class="flex sm:hidden">
                        <div class="flex-col justify-center items-center gap-5">
                            <button
                                class="text-base text-light-gray font-medium leading-100 border hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer px-5 py-3 rounded-lg">Login</button>
                            <button
                                class="bg-light-pink text-white border-transparent text-base font-medium leading-100 px-5 py-3 rounded-lg hover:bg-transparent border hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">Sign
                                Up</button>
                        </div>
                    </li>
                </ul>
                <div class="sm:flex hidden justify-center items-center gap-5">
                    <button
                        class="text-base text-light-gray font-medium leading-100 border hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer px-5 py-3 rounded-lg">Login</button>
                    <button
                        class="bg-light-pink text-white border-transparent text-base font-medium leading-100 px-5 py-3 rounded-lg hover:bg-transparent border hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer text-nowrap">Sign
                        Up</button>
                </div>
                <div id="hamburgerToggle" class="hamburger cursor-pointer block lg:hidden" :class="{ active }"
                    @click="toggle">
                    <svg viewBox="0 0 32 32"
                        class="sm:h-16 h-10 transition-transform duration-600 ease-in-out relative z-[999]"
                        :class="{ '-rotate-45': active }">
                        <path
                            d="M27 10 13 10C10.8 10 9 8.2 9 6 9 3.5 10.8 2 13 2 15.2 2 17 3.8 17 6L17 26C17 28.2 18.8 30 21 30 23.2 30 25 28.2 25 26 25 23.8 23.2 22 21 22L7 22"
                            class="line line-top-bottom" :style="topBottomStyle" />
                        <path d="M7 16 27 16" class="line" />
                    </svg>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { computed, ref } from 'vue'
const open = ref(false)

const links = [
    { name: 'Home', path: '#home' },
    { name: 'About', path: '#about' },
    { name: 'Features', path: '#features' },
    { name: 'Menu', path: '#menu' },
    { name: 'Contact', path: '#contact' },
]
const active = ref(false)

function toggle() {
    active.value = !active.value
    open.value = !open.value
}
function toggleByNavLinks() {
    open.value = false
    active.value = false
}

const topBottomStyle = computed(() =>
    active.value
        ? {
            strokeDasharray: '20 300',
            strokeDashoffset: '-32.42',
        }
        : {
            strokeDasharray: '12 63',
            strokeDashoffset: '0',
        },
)

</script>
<style scoped>
.line {
    fill: none;
    stroke: #FFAA94;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 3;
    transition:
        stroke-dasharray 600ms cubic-bezier(0.4, 0, 0.2, 1),
        stroke-dashoffset 600ms cubic-bezier(0.4, 0, 0.2, 1);
}
</style>