<script setup>
import { ref } from "vue";
import { useProductStore } from "@/stores/product.js";

const message = ref("this is homepage");

const product = useProductStore();
</script>

<template>
   <main>
      <div class="about">
         <h1 class="font-bold text-4xl text-green-500">{{ message }}</h1>
      </div>
   </main>
</template>
