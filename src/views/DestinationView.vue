<script setup>
import background from '@/assets/img/destination-bg.jpg';
import moonimg from '@/assets/img/moon-image.png';
import marsimg from '@/assets/img/mars-image.png';
import titanimg from '@/assets/img/titan-image.png';
import europaimg from '@/assets/img/europa-image.png';
import { RouterLink } from 'vue-router';
import { ref } from 'vue';

const img = ref('moonimg');

// const isActive = (img) => {
//     if (img)
// }

const moon = () => {
    img.value = 'moonimg';
}

const mars = () => {
    img.value = 'marsimg';
}
const europa = () => {
    img.value = 'europaimg';
}
const titan = () => {
    img.value = 'titanimg';
}

const rsh = () => {
    switch (img.value) {
        case 'moonimg':
            return 'MOON'
        case 'marsimg':
            return 'MARS'
        case 'europaimg':
            return 'EUROPA'
        case 'titanimg':
            return 'TITAN'
    }
}
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
        <div class="right-side mt-120">
            <div class="buttons text-[25px]">
                <button class="mr-8 cursor-pointer transition duration-200 ease-out hover:text-green-400" @click="moon">
                    MOON
                </button>
                <button class="mr-8 cursor-pointer transition duration-200 ease-out hover:text-green-400" @click="mars">
                    MARS
                </button>
                <button class="mr-8 cursor-pointer transition duration-200 ease-out hover:text-green-400" @click="europa">
                    EUROPA
                </button>
                <button class="mr-8 cursor-pointer transition duration-200 ease-out hover:text-green-400" @click="titan">
                    TITAN
                </button>
            </div>
            <div class="right-side-heading mt-10">
                {{rsh()}}
            </div>
            <div class="right-side-description text-[18px] text-blue-200 max-w-110">
                See our planet as you’ve never seen it before. A perfect relaxing trip away to help regain perspective and come back refreshed. While you’re there, take in some history by visiting the Luna 2 and Apollo 11 landing sites.
            </div>
            <div class="line w-112 h-[0.1px] mt-3 bg-zinc-400"></div>
            <div class="flex mt-3 justify-between">
                <div class="distance">
                    <div class="d-heading text-blue-200">
                        AVG. DISTANCE
                    </div>
                    <div class="d-data mt-1 text-4xl">
                        384,400 KM
                    </div>
                </div>
                <div class="travel-time">
                    <div class="d-heading text-blue-200">
                        EST. TRAVEL TIME
                    </div>
                    <div class="d-data mt-1 text-4xl">
                        3 DAYS
                    </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>
