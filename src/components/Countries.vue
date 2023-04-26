
<script setup>
import { advancePositionWithClone } from '@vue/compiler-core';
import axios from 'axios'
import FlagCards from '../components/FlagCards.vue'
// import api from '../api.json'
import { ref } from 'vue';
import SingleCountry from './SingleCountry.vue';
let getApi = ref([]);
axios.get('https://restcountries.com/v3.1/all?fields=name,flags').then((res) => {
  getApi.value = res.data
})

// getApi.value= api
</script>
<template>
    <div class="feature-1 py-6 md:py-12">
    <div class="container px-4 mx-auto">
    <div class="grid grid-cols-4 gap-4 rounded-3xl">
      <div v-for="(flag, index) in getApi" :key="index">
     <SingleCountry :countryName="flag.name.official" :image="flag.flags.png"/>
      </div>
    </div>
    </div>
    </div>
</template>