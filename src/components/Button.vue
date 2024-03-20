<template>
    
    <button @click="$emit('cambiar')">{{ title }}</button>
</template>

<script setup>

const props = defineProps({
    title: {
        type: String,
        required: true,

    },
    value: {
        type: Number,
        
    },
})

</script>