<script setup>
import { advancePositionWithClone } from '@vue/compiler-core';
import axios from 'axios'
import Header from '../components/Header.vue'
import FlagCards from '../components/FlagCards.vue'
// import api from '../api.json'
import { ref } from 'vue';
import Countries from '../components/Countries.vue';
let getApi = ref([]);
axios.get('https://restcountries.com/v3.1/all?fields=name,flags').then((res) => {
  getApi.value = res.data
})
// getApi.value= api
</script>
<template>
<section>
  <Header />
  <div class="feature-1 py-6 md:py-12">
  <div class="container px-4 mx-auto">
    <div class="flex -mx-4">
      <div class="px-4 text-center md:w-10/12 xl:w-8/12 mx-auto">
        <h1 class="mb-4 text-4xl font-medium">Countery flags</h1>
        <p class="mb-4 text-l">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
        <RouterLink to="./about" class="border-2 border-solid border-indigo-600 rounded py-2 px-12 text-xl text-indigo-600 hover:bg-indigo-600 hover:text-white mt-4 transition-color duration-300">Learn More</RouterLink>
      </div>
    </div>
    <div class="md:flex md:-mx-4 mt-12 md:pt-4">
      <FlagCards name="Iran" description="Lorem Ipsum" logo="https://flagcdn.com/ir.svg" />
      <FlagCards name="USA" description="Lorem Ipsum" logo="https://flagcdn.com/us.svg"/>
      <FlagCards name="Italy" description="Lorem Ipsum" logo="https://flagcdn.com/it.svg"/>
      <FlagCards name="German" description="Lorem Ipsum"  logo="https://flagcdn.com/de.svg"/>
    </div>
  </div>
</div>
<Countries/>
</section>
</template>
