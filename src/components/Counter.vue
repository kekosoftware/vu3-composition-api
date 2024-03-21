<template>
    <div>
        <h3>Valor: {{ count }}</h3>

        <Button @cambiar="aumentar" title="Aumentar" />
        <Button @cambiar="disminuir" title="Disminuir"/>
    
        <h4>IVA (21%): {{ iva }}%</h4>
    </div>
    
</template>

<script setup>
import { defineProps } from "vue";
import Button from './Button.vue';
import { useCounter } from '../composables/useCounter'

const props = defineProps({
    initialValue: {
        type: Number,
        default: 15
    }
})

const { count, aumentar, disminuir, iva } = useCounter(props.initialValue)

// composables




</script>