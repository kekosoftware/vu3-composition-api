<template>
    <label for="">
        Tecnología #{{ numero }}&nbsp;
    </label>
    <input type="text" v-model="formulario.nombre[numero -1]">
    <select v-model="formulario.nivel[numero -1]" name="nivel">
        <option value="" disabled>Seleccioina un nivel</option>
        <option value="Basico">Basico</option>
        <option value="Intermedio">Intermedio</option>
        <option value="Avanzado">Avanzado</option>
    </select>
</template>

<script setup>
    // import { defineProps } from 'vue';
    import { onUnmounted } from 'vue';
    
    const { numero, formulario } = defineProps(["numero", "formulario"]);

    onUnmounted( () => {
        formulario.nombre.pop(numero -1),
        formulario.nivel.pop(numero -1)
    })

</script>