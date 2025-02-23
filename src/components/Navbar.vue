<script setup>
import logo from '@/assets/shared/logo.svg';
import { RouterLink, useRoute } from 'vue-router';

const isActive = (Route) => {
    const route = useRoute()
    return route.path === Route
}
</script>

<template>
    <div class="navbar flex w-screen justify-between items-center mt-5 absolute bg-none backdrop-blur-sm z-50">
        <RouterLink to="/">
        <img class="h-12 w-auto ml-15" :src="logo" alt="Space tourism">    
        </RouterLink>
        <div class="link flex items-center w-176 h-25 mr-37 justify-evenly text-white text-2xl">
            <RouterLink to="/" :class="[isActive('/') ? 'text-green-400 hover:text-green-600' : 'text-white hover:text-green-400',  'transition', 'duration-200', 'ease-out',]">
                00
                HOME
            </RouterLink>
            <RouterLink to="/destination" :class="[isActive('/destination') ? 'text-green-400 hover:text-green-600' : 'text-white hover:text-green-400',  'transition', 'duration-200', 'ease-out',]">
                01
                DESTINATION
            </RouterLink>
            <RouterLink to="/crew" :class="[isActive('/crew') ? 'text-green-400 hover:text-green-600' : 'text-white hover:text-green-400',  'transition', 'duration-200', 'ease-out',]">
                02
                CREW
            </RouterLink>
            <RouterLink to="/technology" :class="[isActive('/technology') ? 'text-green-400 hover:text-green-600' : 'text-white hover:text-green-400',  'transition', 'duration-200', 'ease-out',]">
                03
                TECHNOLOGY
            </RouterLink>
        </div>
    </div>
</template>
