<script setup>
import { RouterLink } from 'vue-router';
import background from '@/assets/img/home-bg.jpg'
</script>

<template>
  <div class="relative w-screen h-screen">
    <img :src="background" class="absolute top-0 left-0 w-full h-full object-cover" />
  </div>
</template>
