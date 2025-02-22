<script setup>
import background from '@/assets/img/destination-bg.jpg';
import moonimg from '@/assets/img/moon-image.png';
import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="relative w-screen h-screen">
    <img :src="background" class="absolute top-0 left-0 w-full h-full object-cover" />
    <div class="mb-10 ml-40 absolute flex items-center text-white text-3xl h-105 w-277 justify-between">
        <div class="left-side">
            <div class="flex mb-15">
                <div class="number font-bold text-zinc-500">                
                01
                </div>
                <div class="destination-heading ml-5">
                    PICK YOUR DESTINATION
                </div>
            </div>
            <img :src="moonimg" alt="Space" class="absolute w-110 h-110 ml-3">
        </div>
    </div>
  </div>
</template>
