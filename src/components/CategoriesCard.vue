<script setup>
defineProps({
   id: Number,
   title: String,
   image: String,
   count: Number,
});
</script>

<template>
   <div class="w-full px-1 my-2 md:w-1/2 lg:my-4 lg:px-4 lg:w-1/4">
      <div class="overflow-hidden border border-gray-200 rounded-xl">
         <router-link :to="'/categories/' + id">
            <div class="m-4 overflow-hidden rounded-xl">
               <img :alt="'Thumbnail ' + title" class="block w-full h-auto" :src="image" />
            </div>
         </router-link>

         <header class="px-4 mb-4 leading-tight">
            <router-link :to="'/categories/' + id">
               <h1 class="text-lg font-semibold text-black no-underline hover:underline">
                  {{ title }}
               </h1>
            </router-link>
            <span class="block text-sm font-light text-gray-500 no-underline">{{ count }} items </span>
         </header>
      </div>
   </div>
</template>
