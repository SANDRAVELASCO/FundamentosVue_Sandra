<script setup>
import { ref } from 'vue'

const Bienvenida = ref ("Bienvenida a la sección de condicionales")
const nombre = ref ("Sandra Gabriela")
const Apellidos = ref ("Velasco Guzman")
//defineProps({
  //msg: String,
//})
</script>

<template>
  <div class="container">
    <h2 class="text-center">{{ Bienvenida }}</h2>
    <div class="row">
      <div class="col-md-6">
        <h6 class="">{{ nombre }}</h6>
        <h6>{{ Apellidos }}</h6>
      </div>
    </div>
  </div>



</template>

<style scoped>
</style>
