<script setup>
import background from '@/assets/img/crew-bg.jpg'
import hurley from '@/assets/img/hurley.png'
import mark from '@/assets/img/mark.png';
import victor from '@/assets/img/victor.png';
import anousheh from '@/assets/img/anousheh.png';
import { ref } from 'vue';

const img = ref(hurley);

const hurleyBtn = () => {
    img.value = hurley
}

const markBtn = () => {
    img.value = mark
}

const victorBtn = () => {
    img.value = victor
}

const anoushehBtn = () => {
    img.value = anousheh
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
                <div class="role text-[60px] max-w-140 mt-2">
                    {{dynamicName()}}
                </div>
                <div class="rdescription mt-2 max-w-145 text-blue-200 text-[18px]">
                    Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He launched into space for the third time as commander of Crew Dragon Demo-2.
                </div>
                <br>
                <div class="flex mt-10">
                    <button class="h-[20px] w-[20px] bg-zinc-400 aspect-square border rounded-full mr-12 cursor-pointer" @click="hurleyBtn"></button>
                    <button class="h-[20px] w-[20px] bg-zinc-400 aspect-square border rounded-full mr-12 cursor-pointer" @click="markBtn"></button>
                    <button class="h-[20px] w-[20px] bg-zinc-400 aspect-square border rounded-full mr-12 cursor-pointer" @click="victorBtn"></button>
                    <button class="h-[20px] w-[20px] bg-zinc-400 aspect-square border rounded-full mr-12 cursor-pointer" @click="anoushehBtn"></button>
                </div>
            </div>
        <div class="right-side mt-111">
            <img :src="img" alt="" class="h-155">
        </div>
    </div>
  </div>
</template>
