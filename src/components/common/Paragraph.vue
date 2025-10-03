<template>
    <p :class="customClass" class="text-">
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
        default: 'text-lg leading-[30px] font-midium text-light-gray'
    }
})
</script>
