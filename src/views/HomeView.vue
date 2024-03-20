<template>
    <h1>Refs</h1>
    <hr />

    <form action="">
        <div>
            <label for="">
                Tecnologías: 
                <input type="number" min="1" max="5" v-model="formulario.numero">
            </label>
        </div>
        <div v-for="numero in formulario.numero" :key="numero">
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
        </div>
    </form>

    <h3>{{ formulario.nombre }} -  {{ formulario.nivel }}</h3>

</template>

<script setup>
import { reactive } from 'vue'

const formulario = reactive({
    nombre: [],
    nivel: [],
    numero: 1,
})

</script>

<style>

</style>