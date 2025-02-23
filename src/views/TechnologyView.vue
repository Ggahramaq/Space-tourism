<script setup>
import background from '@/assets/img/technology-bg.jpg'
import { RouterLink } from 'vue-router';

</script>

<template>
    <div class="relative w-screen h-screen">
    <img :src="background" class="absolute top-0 left-0 w-full h-full object-cover" />
        <div class="mb-10 ml-40 absolute flex items-center text-white text-3xl h-105 w-277 justify-between">
            <div class="left-side">
                <div class="flex mt-90">
                    <div class="number font-bold text-zinc-500">                
                        03
                    </div>
                    <div class="destination-heading ml-5">
                        SPACE LAUNCH 101
                    </div>
                </div>
                <div class="flex mt-35">
                    <div class="left">
                        <div class="h-15 w-15 aspect-square border rounded-full bg-none border-white text-white"><div class="mt-3 ml-6">
                            1
                        </div>
                    </div>
                        <br>
                        <div class="h-15 w-15 aspect-square border rounded-full bg-none border-white text-white"><div class="mt-3 ml-5">
                            2
                        </div>
                    </div>
                        <br>
                        <div class="h-15 w-15 aspect-square border rounded-full bg-none border-white text-white"><div class="mt-3 ml-5">
                            3
                        </div>
                    </div>
                    </div>
                    <div class="right ml-3">
                        <div class="t-main">THE TERMINOLOGY...</div>
                        <div class="t-head">LAUNCH VEHICLE</div>
                        <div class="t-description">A launch vehicle or carrier rocket is a rocket-propelled vehicle used to carry a payload from Earth's surface to space, usually to Earth orbit or beyond. Our WEB-X carrier rocket is the most powerful in operation. Standing 150 metres tall, it's quite an awe-inspiring sight on the launch pad!</div>
                    </div>
                </div>
            </div>
        <div class="right-side mt-111">
            <!-- <img :src="img" :alt="dynamicName()" class="h-155"> -->
        </div>
    </div>
  </div>
</template>
