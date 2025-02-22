<script setup>
import { RouterLink } from 'vue-router';
import background from '@/assets/img/home-bg.jpg'
</script>

<template>
  <div class="relative w-screen h-screen">
    <img :src="background" class="absolute top-0 left-0 w-full h-full object-cover" />
        <div class="bottom-0 ml-40 absolute flex items-center text-white text-3xl h-155 w-277 justify-between">
            <div class="heading h-100 w-277 mt-45 text-blue-100">
            SO, YOU WANT TO TRAVEL TO
            <br>
            <span class="main-heading text-[150px] text-white">SPACE</span>
            <br>
            <div class="description text-[18px] max-w-137">
                Let’s face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of on the edge of it. Well sit back, and relax because we’ll give you a truly out of this world experience!
            </div>
        </div>
        <RouterLink to="/destination">
            <button class="main-btn w-68 h-68 aspect-square cursor-pointer transition duration-200 ease-out hover:bg-amber-50 bg-white text-black border rounded-full">EXPLORE</button>
        </RouterLink>
    </div>
  </div>
</template>
