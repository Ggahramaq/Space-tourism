<script setup>
import background from '@/assets/img/crew-bg.jpg'
import hurley from '@/assets/img/hurley.png'
import mark from '@/assets/img/mark.png';
import victor from '@/assets/img/victor.png';
import anousheh from '@/assets/img/anousheh.png';
import { ref } from 'vue';

const img = ref(hurley);
const imgstring = ref('hurley');

const hurleyBtn = () => {
    img.value = hurley
    imgstring.value = 'hurley'
}

const markBtn = () => {
    img.value = mark
    imgstring.value = 'mark'
}

const victorBtn = () => {
    img.value = victor
    imgstring.value = 'victor'
}

const anoushehBtn = () => {
    img.value = anousheh
    imgstring.value = 'anousheh'
}

const dynamicRole = () => {
    switch (img.value) {
        case hurley:
            return 'COMMANDER';
        case mark:
            return 'MISSION SPECIALIST';
        case victor:
            return 'PILOT';
        case anousheh:
            return 'FLIGHT ENGINEER'
    };
}

const dynamicName = () => {
    switch (img.value) {
        case hurley:
            return 'DOUGLAS HURLEY';
        case mark:
            return 'MARK SHUTTLEWORTH';
        case victor:
            return 'VICTOR GLOVER';
        case anousheh:
            return 'ANOUSHEH ANSARI'
    };
}

const dynamicDescription = () => {
    switch (img.value) {
        case hurley:
            return 'Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He launched into space for the third time as commander of Crew Dragon Demo-2.';
        case mark:
            return 'Mark Richard Shuttleworth is the founder and CEO of Canonical, the company behind the Linux-based Ubuntu operating system. Shuttleworth became the first South African to travel to space as a space tourist.';
        case victor:
            return 'Pilot on the first operational flight of the SpaceX Crew Dragon to the International Space Station. Glover is a commander in the U.S. Navy where he pilots an F/A-18.He was a crew member of Expedition 64, and served as a station systems flight engineer. ';
        case anousheh:
            return 'Anousheh Ansari is an Iranian American engineer and co-founder of Prodea Systems. Ansari was the fourth self-funded space tourist, the first self-funded woman to fly to the ISS, and the first Iranian in space. '
    };
}

const isActive = (name) => {
    return name === imgstring.value;
}
</script>

<template>
    <div class="relative w-screen h-screen">
    <img :src="background" class="absolute top-0 left-0 w-full h-full object-cover" />
        <div class="mb-10 ml-40 absolute flex items-center text-white text-3xl h-105 w-277 justify-between">
            <div class="left-side">
                <div class="flex mt-105">
                    <div class="number font-bold text-zinc-500">                
                        02
                    </div>
                    <div class="destination-heading ml-5">
                        MEET YOUR CREW
                    </div>
                </div>
                <div class="role text-zinc-400 mt-30">
                    {{dynamicRole()}}
                </div>
                <div class="role text-[60px] mt-2">
                    {{dynamicName()}}
                </div>
                <div class="rdescription mt-2 max-w-145 text-blue-200 text-[18px]">
                    {{dynamicDescription()}}
                </div>
                <br>
                <div class="flex mt-10">
                    <button :class="[isActive('hurley') ? 'bg-zinc-600' : 'bg-zinc-400','border', 'rounded-full', 'mr-12', 'cursor-pointer', 'aspect-square', 'h-[20px]', 'w-[20px]']" @click="hurleyBtn"></button>
                    <button :class="[isActive('mark') ? 'bg-zinc-600' : 'bg-zinc-400','border', 'rounded-full', 'mr-12', 'cursor-pointer', 'aspect-square', 'h-[20px]', 'w-[20px]']" @click="markBtn"></button>
                    <button :class="[isActive('victor') ? 'bg-zinc-600' : 'bg-zinc-400','border', 'rounded-full', 'mr-12', 'cursor-pointer', 'aspect-square', 'h-[20px]', 'w-[20px]']" @click="victorBtn"></button>
                    <button :class="[isActive('anousheh') ? 'bg-zinc-600' : 'bg-zinc-400','border', 'rounded-full', 'mr-12', 'cursor-pointer', 'aspect-square', 'h-[20px]', 'w-[20px]']" @click="anoushehBtn"></button>
                </div>
            </div>
        <div class="right-side mt-111">
            <img :src="img" :alt="dynamicName()" class="h-155">
        </div>
    </div>
  </div>
</template>
