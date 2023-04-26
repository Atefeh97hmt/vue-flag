
<template>
      <div class="px-3 md:w-1/3 mt-6 md:mt-0">
        <div class="feature-box text-center p-4 md:p-6 max-w-sm mx-auto border-2 border-solid border-gray-300 rounded md:h-full">
          <div class="text-xl p-4 w-16 h-16 mx-auto">         

            <img :src="props.logo" alt="">
        
          </div>
          <h5 class="text-xl font-medium mb-4">{{ props.name }}</h5>
          <p class="text-gray-600 mb-3">{{ props.description }}.</p>
        </div>
      </div>
  </template>


<script setup>
  const props = defineProps({
    name: {
      type: String,
      required: true,
      default: ""
    },
    description: {
      type: String,
      required:true
    },

    logo:{
      type:String,
      required:true
    }
  })

</script>