<template>
    <div class="px-5 py-10">
        <div class="max-w-[1180px] mx-auto w-full flex justify-between items-center">
            <h2 class="text-light-pink text-custom-5xl font-semibold leading-[30px]">Restro</h2>
            <div class="flex justify-between items-center gap-10 max-w-[681px] w-full">
                <ul class="flex gap-10">
                    <li v-for="link in links" class="text-base text-light-gray font-medium leading-100" :key="index">
                        <a class="hover:text-light-pink transition-all duration-300 ease-in-out after:absolute relative after:-bottom-1 after:left-1/2 after:-translate-x-1/2 after:w-0 after:h-1 after:rounded-2xl after:bg-light-pink hover:after:w-full after:transition-all after:duration-300 after:ease-in-out" :href="link.path">{{ link.name }}</a>
                    </li>
                </ul>
                <div class="flex justify-center items-center gap-5">
                    <button
                        class="text-base text-light-gray font-medium leading-100 border hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer px-5 py-3 rounded-lg">Login</button>
                    <button
                        class="bg-light-pink text-white text-base font-medium leading-100 px-5 py-3 rounded-lg hover:bg-white border hover:border-light-pink hover:text-light-pink transition-all duration-300 ease-in-out cursor-pointer">Sign
                        Up</button>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
const links = [
    { name: 'Home', path: '#home' },
    { name: 'About', path: '#about' },
    { name: 'Features', path: '#features' },
    { name: 'Menu', path: '#menu' },
    { name: 'Contact', path: '#contact' },
]
</script>