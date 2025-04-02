<template>
    <div class="container bg-light py-4">
      <!-- Título del horario -->
      <h3 class="mt-4 text-center text-white fw-bold p-3 rounded" style="background-color: #6a0dad; border: 3px solid #4b0082;">
        HORARIO DE CLASES DE SISTEMAS
      </h3>
      <!-- Tabla que representa el horario -->
      <table class="table table-bordered text-center" style="background-color: #f8d7ff; border: 2px solid #6a0dad;">
        <thead class="table-dark">
          <tr>
            <th scope="col">Hora</th>
            <th scope="col">Lunes</th>
            <th scope="col">Martes</th>
            <th scope="col">Miércoles</th>
            <th scope="col">Jueves</th>
            <th scope="col">Viernes</th>
          </tr>
        </thead>
        <tbody>
          <!-- Uso de v-for para iterar sobre el arreglo horario y generar filas de la tabla -->
          <tr v-for="(h, index) in horario" :key="index">
            <!-- Celda de la hora -->
            <td class="fw-bold">{{ h.hora_ }}</td>
            <!-- Celdas de cada día de la semana con sus respectivas materias -->
            <td>{{ h.Lunes }}</td>
            <td>{{ h.Martes }}</td>
            <td>{{ h.Miercoles }}</td>
            <td>{{ h.Jueves }}</td>
            <td>{{ h.Viernes }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  // Definición del arreglo que contiene los datos del horario
  const horario = ref([
    { hora_: '7:00 - 9:00', Lunes: 'Desarrollo Ágil', Martes: 'Inteligencia Artificial', Miercoles: 'Desarrollo en la Nube', Jueves: 'Realidad Aumentada', Viernes: 'Administración de Redes' },
    { hora_: '9:00 - 11:00', Lunes: 'Programación Lógica y Funcional', Martes: 'Desarrollo Ágil', Miercoles: 'Inteligencia Artificial', Jueves: 'Desarrollo en la Nube', Viernes: 'Realidad Aumentada' },
    { hora_: '11:00 - 13:00', Lunes: 'Administración de Redes', Martes: 'Programación Lógica y Funcional', Miercoles: 'Desarrollo Ágil', Jueves: 'Inteligencia Artificial', Viernes: 'Desarrollo en la Nube' },
    { hora_: '13:00 - 15:00', Lunes: 'Realidad Aumentada', Martes: 'Administración de Redes', Miercoles: 'Programación Lógica y Funcional', Jueves: 'Desarrollo Ágil', Viernes: 'Inteligencia Artificial' }
  ]);
  </script>