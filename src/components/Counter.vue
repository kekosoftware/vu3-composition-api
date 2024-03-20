<template>
    <center>
        <h3>Valor: {{ count }}</h3>
        <button @click="aumentar">+1</button>
        <button @click="disminuir">-1</button>
    </center>
</template>

<script setup>
import { ref } from "vue";

const count = ref(10)

const aumentar = () => {
    count.value++
}

const disminuir = () => {
    count.value--
}

</script>