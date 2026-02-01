<script setup>
import { ref } from 'vue';
import Stat from './components/Stat.vue';
import CitySelect from './components/CitySelect.vue';

let savedCity = ref("Moscow")
let data  = ref({
    label: "Влажность",
    stat: "90%",
})

const getCity = (city) => {
  console.log(city);
  savedCity.value = city
  data.value.stat = "20%";
}
</script>

<template>
  <main class="main">
    {{ savedCity }}
    <Stat v-bind="data"/>
    <Stat label="Осадки" stat="0%"/>
    <CitySelect @selectCity="getCity"/>
  </main>
</template>

<style scoped>
  .main {
    background: var(--color-bg-main);
    padding: 60px 50px;
    border-radius: 25px;
  }
</style>
