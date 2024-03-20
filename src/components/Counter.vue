<template>
    <div>
        <h3>Valor: {{ count }}</h3>

        <Button @cambiar="aumentar" title="Aumentar" />
        <Button @cambiar="disminuir" title="Disminuir"/>
    
        <h4>IVA (21%): {{ iva }}%</h4>
    </div>
    
</template>

<script setup>
import { ref, computed, defineProps } from "vue";
import Button from './Button.vue';

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