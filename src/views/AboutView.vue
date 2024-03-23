<template>
    <div>
        <counter :initialValue="200" />
        <counter />
    </div>
</template>

<script setup>
import Counter from '@/components/Counter.vue'
import { useLink, useRouter } from 'vue-router';

// const router = useRouter();

// const link = useLink();

// console.log(router, link)

</script>

<style>

</style>