<script setup>
import background from '@/assets/img/technology-bg.jpg';
import lv from '@/assets/img/launchvehicle.jpg';
import sc from '@/assets/img/spacecapsule.jpg';
import sp from '@/assets/img/spaceport.jpg';
import { RouterLink } from 'vue-router';
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
</script>

<template>
    <div class="relative w-screen h-screen">
    <img :src="background" class="absolute top-0 left-0 w-full h-full object-cover" />
        <div class="mb-10 ml-40 absolute flex items-center text-white text-3xl h-105 w-277 justify-between">
            <div class="left-side">
                <div class="flex ml-4 mt-95">
                    <div class="number font-bold text-zinc-500">                
                        03
                    </div>
                    <div class="destination-heading ml-5">
                        SPACE LAUNCH 101
                    </div>
                </div>
                <div class="flex mt-20">
                    <div class="left mt-10">
                        <div class="h-15 w-15 aspect-square border rounded-full bg-none border-white text-white cursor-pointer" @click="lvBtn"><div class="mt-3 ml-6">
                            1
                        </div>
                    </div>
                        <br>
                        <div class="h-15 w-15 aspect-square border rounded-full bg-none border-white cursor-pointer text-white" @click="spBtn"><div class="mt-3 ml-5">
                            2
                        </div>
                    </div>
                        <br>
                        <div class="h-15 w-15 aspect-square border rounded-full bg-none cursor-pointer border-white text-white" @click="scBtn"><div class="mt-3 ml-5">
                            3
                        </div>
                    </div>
                    </div>
                    <div class="right ml-15">
                        <div class="t-main text-[40px] text-zinc-400">THE TERMINOLOGY...</div>
                        <div class="t-head mt-5 text-[65px]">{{imgstring}}</div>
                        <div class="t-description mt-3 text-[27px] text-blue-200 max-w-218">{{showDescription(imgstring)}}</div>
                    </div>
                </div>
            </div>
        <div class="right-side">
            <img :src="img" alt="asd" class="h-120 mt-105 ml-42 border-0 rounded-lg">
        </div>
    </div>
  </div>
</template>
