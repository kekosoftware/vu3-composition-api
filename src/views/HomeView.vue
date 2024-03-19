<template>
    <h1>Refs</h1>
    <hr />

    <form action="">
        <input type="text" v-model="nombre">
        <select v-model="nivel" name="nivel">
            <option value="" disabled>Seleccioina un nivel</option>
            <option value="Basico">Basico</option>
            <option value="Intermedio">Intermedio</option>
            <option value="Avanzado">Avanzado</option>
        </select>
    </form>

    <h3>{{ nombre }} -  {{ nivel }}</h3>

    {{ msg }}
</template>

<script setup>
// Compostion API
import { ref } from 'vue'

const nombre = ref("Vue.js")
const nivel = ref("")


// Option API
// export default {
    // data: () => ({
    //     msg: "uaslf",
    // })
// }
</script>

<style>

</style>