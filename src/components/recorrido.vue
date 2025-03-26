<template>
    <div class="container">
      <h3>Lista de alumnos</h3>
      <ul>
        <li v-for="alumno in alumnos" :key="alumno.id">
          <div class="alumno-info">
            <strong>{{ alumno.nombre }}</strong>
            <span>{{ alumno.apellidos }}</span> - 
            <span>{{ alumno.carrera }}</span> <br>
            <span><strong>Lo que le gusta:</strong> {{ alumno.gusta }}</span> <br>
            <span><strong>Pasatiempo:</strong> {{ alumno.pasatiempo }}</span>
          </div>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        alumnos: [
          { id: 20620165, nombre: 'Sandra', apellidos: 'Lopez', carrera: 'Ingeniería en sistemas computacionales', gusta: 'Programar', pasatiempo: 'Leer libros' },
          { id: 20620166, nombre: 'Gabriela', apellidos: 'Martinez', carrera: 'Administración', gusta: 'Gestionar proyectos', pasatiempo: 'Bailar' },
          { id: 20620167, nombre: 'Velasco', apellidos: 'Perez', carrera: 'ISC', gusta: 'Tecnologías emergentes', pasatiempo: 'Fotografía' },
          { id: 20620168, nombre: 'Carlos', apellidos: 'Hernandez', carrera: 'Ingeniería Civil', gusta: 'Diseñar estructuras', pasatiempo: 'Correr maratones' },
          { id: 20620169, nombre: 'Ana', apellidos: 'Gomez', carrera: 'Psicología', gusta: 'Ayudar a los demás', pasatiempo: 'Cocinar' },
          { id: 20620170, nombre: 'Luis', apellidos: 'Sanchez', carrera: 'Medicina', gusta: 'Investigar enfermedades', pasatiempo: 'Tocar guitarra' },
          { id: 20620171, nombre: 'María', apellidos: 'Fernández', carrera: 'Derecho', gusta: 'Estudiar leyes', pasatiempo: 'Ver películas' },
          { id: 20620172, nombre: 'Juan', apellidos: 'Rodriguez', carrera: 'Arquitectura', gusta: 'Diseñar edificios', pasatiempo: 'Viajar' }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  /* Estilo para el contenedor */
  .container {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f4f4f4;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
  }
  
  /* Estilo para el título */
  h3 {
    font-size: 36px;
    font-family: 'Times New Roman', Times, serif;
    color: #333;
    text-align: center;
    margin-bottom: 20px;
    padding: 10px;
    background-color: #4CAF50; /* Verde */
    border-radius: 15px; /* Borde redondeado */
    color: white;
    border: 2px solid #3e8e41; /* Borde más oscuro del mismo color */
  }
  
  /* Estilo para la lista */
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  /* Estilo para los elementos de la lista */
  li {
    background-color: #2c3e50; /* Gris oscuro */
    color: #ecf0f1; /* Color de texto claro */
    border-radius: 10px;
    padding: 15px;
    margin: 10px 0;
    display: flex;
    flex-direction: column;
    transition: background-color 0.3s ease;
  }
  
  /* Efecto hover */
  li:hover {
    background-color: #34495e; /* Gris un poco más claro */
    cursor: pointer;
  }
  
  /* Estilo para los nombres de los alumnos */
  .alumno-info {
    display: flex;
    flex-direction: column;
    width: 100%;
  }
  
  /* Estilo para el nombre */
  .alumno-info strong {
    font-size: 18px;
    color: #1abc9c; /* Verde claro */
    margin-right: 10px;
  }
  
  /* Estilo para los apellidos y carrera */
  .alumno-info span {
    font-size: 16px;
    color: #ecf0f1; /* Color claro */
  }
  
  /* Estilo para el texto en hover */
  li:hover .alumno-info strong,
  li:hover .alumno-info span {
    color: #fff;
  }
  </style>
  