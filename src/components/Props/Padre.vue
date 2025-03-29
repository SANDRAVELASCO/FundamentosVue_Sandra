<script setup>
import Hijo1 from './Hijo1.vue';
import Hijo2 from './Hijo2.vue';
</script>

<template>
    <div class="container mt-5">
        <div class="card p-4 shadow">
            <h1 class="text-center text-primary">Soy el componente Padre</h1>
            <div class="row mt-4">
                <div class="col-md-6">
                    <Hijo1 class="border p-3 rounded bg-light" edad="23" Carrera="Ingeniería en sistemas"/>
                </div>
                <div class="col-md-6">
                    <Hijo2 class="border p-3 rounded bg-light" edad="20" Carrera="Ingeniería civil"/>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
</style>
