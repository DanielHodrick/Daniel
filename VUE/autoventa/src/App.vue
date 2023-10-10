<template>
  <div class="nav-bar"></div>
  <article class="product-display">
    <div class="product-container">
      <div class="product-image">
        <img :src="img" alt="NISSAN JUKE">
      </div>
      <div class="product-info">
        <h1>{{ prod }} </h1>
        <!--if-->
        <!--<p v-if="disponible">Disponible</p>
        <p v-else="">Agotado</p>-->
        <p v-if="disponible!=0" style="color: red;">Disponible </p>
        <p v-else="">Agotado</p>
        <p v-if="stock>10">Variedad de colores y equipamientos</p>
        <p v-else-if="stock<=10 && stock>0">Pocas unidades adquiera el suyo</p>
        <p v-else>Agotado</p>
        <ul>
          <li v-for="d in detalles"> {{ d }}</li>
        </ul>
      </div>

    </div>
  </article>
</template>

<script setup>
const img = './src/assets/images/blanco.png'
const prod = "Automovil"
//--vondicionante v-if
const disponible = true;

//decalracion de stock
const stock=5;
//construccion de detalles
 const detalles = ["AT","2300 cc","VXR45","OT","113 Nm"]
</script>

<style scoped></style>