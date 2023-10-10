<template>
  <!--CONCATENACION DE CANDENAS-->
  <h1>{{ prod.toUpperCase() + " otro texto" }}</h1>
  <!--USO DE IF TERNARIO-->
  <h1>{{ esValido ? "valido" : "no Valido"
  }}</h1>
  <!--APLICACION DE COLOR A UN H1-->
  <h1 :style="color">{{ prod.toUpperCase() + " otro texto" }}</h1>
  <h1 v-bind:style="color2">{{ prod.toUpperCase() + " otro texto" }}</h1>
  <div>

  </div>
</template>

<script setup>
const prod = "Automovil"
//validacion de parametro booleano esvalido
const esValido = true;
const color = "color: red";
const color2 = "color: blue"; 
</script>

<style scoped></style>