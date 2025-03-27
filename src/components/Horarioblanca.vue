<template>
    <div class="container">
      <h3 class="mt-4">Horario de clases de sistemas</h3>
      <table class="table">
        <thead>
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
          <tr v-for="(s, index) in sistemas" :key="index">
            <td>{{ s.hora }}</td>
            <td>{{ s.lunes }}</td>
            <td>{{ s.martes }}</td>
            <td>{{ s.miercoles }}</td>
            <td>{{ s.jueves }}</td>
            <td>{{ s.viernes }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const sistemas = ref([
    { hora: '11:00-1:00', lunes: 'Lenguajes y Automatas I', martes: 'Lenguajes de interfaz', miercoles: 'Lenguajes y Autómatas I', jueves: 'Libre', viernes: 'Lenguajes y Autómatas I' },
    { hora: '1:00-3:00', lunes: 'Taller de sistemas operativos', martes: 'Redes de computadoras', miercoles: 'Taller de sistemas operativos', jueves: 'Redes de computadoras', viernes: 'Programación web - Administración de bases de datos' },
    { hora: '3:00-5:00', lunes: 'Ingeneria de software', martes: 'Administracion de base de datos', miercoles: 'Administracion de base de datos', jueves: 'Ingeneria de software', viernes: 'Ingeneria de software-Redes de computadoras' },
    { hora: '5:00-7:00', lunes: 'Libre', martes: 'Programacion web', miercoles: 'Lenguajes de interfaz', jueves: 'Programacion web', viernes: 'Libre' }
  ]);
  </script>

  
  