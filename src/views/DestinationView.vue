<script setup>
import background from '@/assets/img/destination-bg.jpg';
import moonimg from '@/assets/img/moon-image.png';
import marsimg from '@/assets/img/mars-image.png';
import titanimg from '@/assets/img/titan-image.png';
import europaimg from '@/assets/img/europa-image.png';
import { ref } from 'vue';

const img = ref(moonimg);
const imgstring = ref('moon');

const isActive = (image) => {
    return image == imgstring.value
}

const moon = () => {
    img.value = moonimg;
    imgstring.value = 'moon'
}

const mars = () => {
    img.value = marsimg;
    imgstring.value = 'mars'
}
const europa = () => {
    img.value = europaimg;
    imgstring.value = 'europa'
}
const titan = () => {
    img.value = titanimg;
    imgstring.value = 'titan'
}

const rsh = () => {
    switch (img.value) {
        case moonimg:
            return 'MOON'
        case marsimg:
            return 'MARS'
        case europaimg:
            return 'EUROPA'
        case titanimg:
            return 'TITAN'
    }
}

const rsd = () => {
    switch (img.value) {
        case moonimg:
            return 'See our planet as you’ve never seen it before. A perfect relaxing trip away to help regain perspective and come back refreshed. While you’re there, take in some history by visiting the Luna 2 and Apollo 11 landing sites.'
        case marsimg:
            return 'Don’t forget to pack your hiking boots. You’ll need them to tackle Olympus Mons, the tallest planetary mountain in our solar system. It’s two and a half times the size of Everest!'
        case europaimg:
            return 'The smallest of the four Galilean moons orbiting Jupiter, Europa is a winter lover’s dream. With an icy surface, it’s perfect for a bit of ice skating, curling, hockey, or simple relaxation in your snug wintery cabin.'
        case titanimg:
            return 'The only moon known to have a dense atmosphere other than Earth, Titan is a home away from home (just a few hundred degrees colder!). As a bonus, you get striking views of the Rings of Saturn.'
    }
}

const dd = () => {
    switch (img.value) {
        case moonimg:
            return '384,000 KM'
        case marsimg:
            return '225 MIL. KM'
        case europaimg:
            return '628 MIL. KM'
        case titanimg:
            return '1.6 BIL. KM'
    }
}

const td = () => {
    switch (img.value) {
        case moonimg:
            return '3 DAYS'
        case marsimg:
            return '9 MONTHS'
        case europaimg:
            return '3 YEARS'
        case titanimg:
            return '7 YEARS'
    }
}

const lsimg = () => {
    return img.value;
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
            <img :src="lsimg()" alt="Space" class="absolute w-110 h-110 ml-3">
        </div>
        <div class="right-side mt-120">
            <div class="buttons text-[25px]">
                <button :class="[isActive('moon') ? 'text-green-400 hover:text-green-600' : 'hover:text-green-400', 'mr-8', 'cursor-pointer', 'transition', 'duration-200', 'ease-out']" @click="moon">
                    MOON
                </button>
                <button :class="[isActive('mars') ? 'text-green-400 hover:text-green-600' : 'hover:text-green-400', 'mr-8', 'cursor-pointer', 'transition', 'duration-200', 'ease-out']" @click="mars">
                    MARS
                </button>
                <button :class="[isActive('europa') ? 'text-green-400 hover:text-green-600' : 'hover:text-green-400', 'mr-8', 'cursor-pointer', 'transition', 'duration-200', 'ease-out']" @click="europa">
                    EUROPA
                </button>
                <button :class="[isActive('titan') ? 'text-green-400 hover:text-green-600' : 'hover:text-green-400', 'mr-8', 'cursor-pointer', 'transition', 'duration-200', 'ease-out']" @click="titan">
                    TITAN
                </button>
            </div>
            <div class="right-side-heading mt-10">
                {{rsh()}}
            </div>
            <div class="right-side-description text-[18px] text-blue-200 max-w-110">
                {{rsd()}}
            </div>
            <div class="line w-112 h-[0.1px] mt-3 bg-zinc-400"></div>
            <div class="flex mt-3 justify-between">
                <div class="distance">
                    <div class="d-heading text-blue-200">
                        AVG. DISTANCE
                    </div>
                    <div class="d-data mt-1 text-4xl">
                        {{dd()}}
                    </div>
                </div>
                <div class="travel-time">
                    <div class="d-heading text-blue-200">
                        EST. TRAVEL TIME
                    </div>
                    <div class="d-data mt-1 text-4xl">
                        {{td()}}
                    </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>
