<template>
    <p :class="customClass" class="text-lg leading-[30px] font-midium text-light-gray">
        <slot>{{ text }}</slot>
    </p>
</template>

<script setup>
defineProps({
    text: {
        type: String,
        default: ''
    },
    customClass: {
        type: String,
        default: ''
    }
})
</script>
