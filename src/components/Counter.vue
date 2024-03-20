<template>
    <center>
        <h3>Valor: {{ count }}</h3>
        <button @click="aumentar">+1</button>
        <button @click="disminuir">-1</button>

        <h4>IVA (21%): {{ porcentaje }}%</h4>
    </center>
</template>

<script setup>
import { ref, computed } from "vue";

const count = ref(10)

const aumentar = () => {
    count.value++
}

const disminuir = () => {
    count.value--
}

const porcentaje = computed(() => 
    count.value * 1.21
)

</script>