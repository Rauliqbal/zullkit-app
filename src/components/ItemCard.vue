<script setup>
defineProps({
   title: String,
   description: String,
   image: String,
});
</script>

<template>
   <div class="w-full px-1 my-1 md:w-1/2 lg:my-4 lg:px-4 lg:w-1/3">
      <div class="overflow-hidden border border-gray-200 rounded-xl">
         <router-link to="/product">
            <div class="m-4 overflow-hidden rounded-xl">
               <img :alt="'Thumbnail ' + title" class="block w-full h-auto" :src="'/src/assets/img/' + image" />
            </div>
         </router-link>

         <header class="px-4 mb-4 leading-tight">
            <h1 class="text-lg">
               <router-link to="/product" class="font-semibold text-black no-underline hover:underline">{{ title }}</router-link>
            </h1>
            <span class="block text-sm font-light text-gray-500 no-underline">{{ description }}</span>
         </header>
      </div>
   </div>
</template>
