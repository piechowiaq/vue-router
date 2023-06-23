<script setup>
import {useRoute} from "vue-router"

const route = useRoute()

import cars from "../data/cars.json"

const car = cars.find(car => car.id === parseInt(route.params.id))


</script>

<template>
  <div>
    <h1>
      Contact Info
      <p>{{car.contact.dealer}}</p>
      <p>{{car.contact.number}}</p>
    </h1>
  </div>
</template>



<style scoped>

</style>