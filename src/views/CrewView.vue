<script setup>
import background from '@/assets/img/technology-bg.jpg';
import lv from '@/assets/img/launchvehicle.jpg';
import sc from '@/assets/img/spacecapsule.jpg';
import sp from '@/assets/img/spaceport.jpg';
import { ref } from 'vue';

const img = ref(lv);
const imgstring = ref('LAUNCH VEHICLE')

const lvBtn = () => {
    img.value = lv
    imgstring.value = 'LAUNCH VEHICLE'
}

const scBtn = () => {
    img.value = sc
    imgstring.value = 'SPACE CAPSULE'
}

const spBtn = () => {
    img.value = sp
    imgstring.value = 'SPACEPORT'
}

const showDescription = (name) => {
    switch (name) {
        case 'LAUNCH VEHICLE':
            return `A launch vehicle or carrier rocket is a rocket-propelled vehicle used to carry a payload from Earth's surface to space, usually to Earth orbit or beyond. Our WEB-X carrier rocket is the most powerful in operation. Standing 150 metres tall, it's quite an awe-inspiring sight on the launch pad!`;
        case 'SPACEPORT':
            return `A spaceport or cosmodrome is a site for launching (or receiving) spacecraft, by analogy to the seaport for ships or airport for aircraft. Based in the famous Cape Canaveral, our spaceport is ideally situated to take advantage of the Earth’s rotation for launch.`;
        case 'SPACE CAPSULE':
            return `A space capsule is an often-crewed spacecraft that uses a blunt-body reentry capsule to reenter the Earth's atmosphere without wings. Our capsule is where you'll spend your time during the flight. It includes a space gym, cinema, and plenty of other activities to keep you entertained.`;
    }
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
                <div class="flex ml-4 mt-75">
                    <div class="number font-bold text-zinc-500">                
                        03
                    </div>
                    <div class="destination-heading ml-5">
                        SPACE LAUNCH 101
                    </div>
                </div>
                <div class="flex mt-30">
                    <div class="left">
                        <div :class="[isActive('LAUNCH VEHICLE') ? 'bg-white text-black hover:bg-transparent hover:text-blue-400' : 'hover:bg-blue-400 hover:text-black border-white text-white bg-transparent', 'transition', 'duration-200', 'ease-out', 'h-15', 'w-15', 'aspect-square', 'border', 'rounded-full', 'cursor-pointer']" @click="lvBtn"><div class="mt-3 ml-6">
                            1
                        </div>
                    </div>
                        <br>
                        <div :class="[isActive('SPACEPORT') ? 'bg-white text-black hover:bg-transparent hover:text-blue-400' : 'hover:bg-white hover:text-black border-white text-white bg-none', 'transition', 'duration-200', 'ease-out', 'h-15', 'w-15', 'aspect-square', 'border', 'rounded-full', 'cursor-pointer']" @click="spBtn"><div class="mt-3 ml-5">
                            2
                        </div>
                    </div>
                        <br>
                        <div :class="[isActive('SPACE CAPSULE') ? 'bg-white text-black hover:bg-transparent hover:text-blue-400' : 'hover:bg-white hover:text-black border-white text-white bg-none', 'transition', 'duration-200', 'ease-out', 'h-15', 'w-15', 'aspect-square', 'border', 'rounded-full', 'cursor-pointer']" @click="scBtn"><div class="mt-3 ml-5">
                            3
                        </div>
                    </div>
                    </div>
                    <div class="right ml-15">
                        <div class="t-main mt-[-10px] text-[40px] text-zinc-400 absolute">THE TERMINOLOGY...</div>
                        <div class="t-head mt-11 text-[65px] absolute">{{imgstring}}</div>
                        <div class="t-description mt-31 text-[23px] text-blue-200 absolute max-w-160">{{showDescription(imgstring)}}</div>
                    </div>
                </div>
            </div>
        <div class="right-side">
            <img :src="img" alt="asd" class="h-120 mt-110 ml-120 border-0 rounded-lg">
        </div>
    </div>
  </div>
</template>
