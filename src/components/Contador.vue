<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <h1>Hola Mundo</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Decrementar</button>
</template>

<script setup>
  import {ref} from 'vue';
  const contador = ref(0);
  const incrementar = () =>{
    contador.value++;
  }
  const decrementar = () =>{
    contador.value--;
  }
</script>

<style scoped>
.p{
  color: rgb(68, 0, 255);
}
</style>


