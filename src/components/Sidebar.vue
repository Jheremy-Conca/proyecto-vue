<!-- eslint-disable vue/multi-word-component-names -->
<template>
 <div class="sidebar">
  <h2>Bienvenido</h2>
  <h3>Nombre: {{nombre}}</h3>
  <h3>Email: {{ email }}</h3>

  <ul>
    <li><router-link to = "/contador">Contador</router-link></li>
    <li> <router-link to = "/lista-de-tareas">Lista de Tareas</router-link></li>
    <li> <router-link to = "/registrar">Registrar</router-link></li>
</ul>
 </div>
</template>

<script setup>
import { useRegistrarStore } from '@/modules/stores/registrarStore';
import { ref, watch } from 'vue';

const registrarStore = useRegistrarStore();
const nombre = ref (registrarStore.nombre.value);
const email = ref (registrarStore.email.value);

watch (() => registrarStore.nombre, (newValor) =>{
  nombre.value = newValor;
});

watch (() => registrarStore.email, (newValor) =>{
  email.value = newValor;
});



</script>

<style>
.sidebar{
  width: 200px;
  background-color: #f0f0f0;
}

</style>
