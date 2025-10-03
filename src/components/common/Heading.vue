<template>
    <h2 :class="customClass" class="text-black font-bold leading-100">
        {{ text }}
    </h2>
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
