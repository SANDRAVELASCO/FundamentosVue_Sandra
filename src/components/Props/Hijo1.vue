<script setup>
import { ref } from 'vue'

defineProps({
    edad: String,
    Carrera: String,
})
</script>
<template>
    <h6>Soy el componente Hijo 1</h6>
    <p>{{ edad }}</p>
    <p>{{ Carrera }}</p>
</template>
<style scoped>
</style>
