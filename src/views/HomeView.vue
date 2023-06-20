<script setup>

import cars from "../data/cars.json"
import {RouterLink} from "vue-router";


</script>

<template>
  <div>
    <h1>Home View</h1>
    <div class="cars">
      <RouterLink v-for="car in cars" :key="car.id" :to="`/cars/${car.id}`">
        {{car.name}}
      </RouterLink>
    </div>
  </div>
</template>

<style scoped>

.cars {
  display: flex;
}

a {
  text-decoration: none;
  color: #2c3e50;
  width: 100%;
  box-shadow: 1px 1px 10px black;
  margin: 10px;
}

</style>