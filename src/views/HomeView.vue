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
            <Inputs :numero="numero" :formulario="formulario" />
        </div>
    </form>

    <h3>{{ formulario.nombre }} -  {{ formulario.nivel }}</h3>

</template>

<script setup>
import { reactive } from 'vue'
import Inputs from "../components/Inputs.vue"

const formulario = reactive({
    nombre: [],
    nivel: [],
    numero: 1,
})

</script>

<style>

</style>