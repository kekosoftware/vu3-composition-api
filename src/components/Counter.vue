<template>
    <div>
        <h3>Valor: {{ count }}</h3>
        <button @click="aumentar">+1</button>
        <button @click="disminuir">-1</button>
    
        <h4>IVA (21%): {{ iva }}%</h4>
    </div>
    
</template>

<script setup>
import { ref, computed, defineProps } from "vue";

const props = defineProps({
    initialValue: {
        type: Number,
        default: 15
    }
})

const count = ref(props.initialValue)

const aumentar = () => {
    count.value++
}

const disminuir = () => {
    count.value--
}

const iva = computed(() => 
    count.value * 1.21
)

</script>