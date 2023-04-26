
<template>
   <div class=" relative text-center bg-violet-100 rounded-3xl shadow-lg duration-75 hover:bg-violet-400 duration-75">
          <div class=" inset-0  w-full ">
            <img class="flag-image-wrap rounded-3xl p-1.5 duration-75 hover:scale-90 duration-75" :src="props.image" />
            <div class="flex flex-col flex-1 p-4 mx-auto">
              <p class="text-ml font-bold tracking-normal text-gray-900 tk-brandon-grotesque">{{ props.countryName }}</p>
            </div>
          </div>
        </div>
</template>


<script setup>
  const props = defineProps({
    countryName: {
      type: String,
      required:true,
      default: ""
    },

    image:{
      type:String,
      required:true
    }
  })

</script>