<!-- eslint-disable vue/multi-word-component-names -->
<template>
 <div class="sidebar">
  <h2>Bienvenido</h2>
  <h3>Nombre: {{registrarStore.nombre}}</h3>
  <h3>Email: {{ registrarStore.email }}</h3>

  <ul>
    <li><router-link to = "/contador">Contador</router-link></li>
    <li> <router-link to = "/lista-de-tareas">Lista de Tareas</router-link></li>
    <li> <router-link to = "/registrar">Registrar</router-link></li>
</ul>
 </div>
</template>

<script setup>
import { useRegistrarStore } from '@/modules/stores/registrarStore';


const registrarStore = useRegistrarStore();




</script>

<style>

.sidebar{
  margin-top: 20px;
  width: 200px;
  background-color: #f0f0f0;
}

</style>
