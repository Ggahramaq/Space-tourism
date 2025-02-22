<script setup>
import logo from '@/assets/shared/logo.svg';
import { RouterLink } from 'vue-router';
</script>

<template>
    <div class="navbar flex w-screen justify-between items-center mt-5 absolute bg-none backdrop-blur-sm z-50">
        <RouterLink to="/">
        <img class="h-12 w-auto ml-15" :src="logo" alt="Space tourism">    
        </RouterLink>
        <div class="link flex items-center w-176 h-25 mr-37 justify-evenly text-white text-2xl">
            <RouterLink to="/" class="transition duration-200 ease-out hover:text-green-400">
                00
                HOME
            </RouterLink>
            <RouterLink to="/destination" class="transition duration-200 ease-out hover:text-green-400">
                01
                DESTINATION
            </RouterLink>
            <RouterLink to="/crew" class="transition duration-200 ease-out hover:text-green-400">
                02
                CREW
            </RouterLink>
            <RouterLink to="/technology" class="transition duration-200 ease-out hover:text-green-400">
                03
                TECHNOLOGY
            </RouterLink>
        </div>
    </div>
</template>