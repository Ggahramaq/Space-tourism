<script setup>
import background from '@/assets/img/destination-bg.jpg';
import moonimg from '@/assets/img/moon-image.png';
import { RouterLink } from 'vue-router';
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
        <div class="right-side mt-90">
            <div class="buttons cursor-pointer">
                MOON
                MARS
                EUROPA
                TITAN
            </div>
            <br>
            <div class="right-side-heading">
                MOON
            </div>
            <br>
            <!-- <div class="right-side-description">
                See our planet as you’ve never seen it before. A perfect relaxing trip away to help regain perspective and come back refreshed. While you’re there, take in some history by visiting the Luna 2 and Apollo 11 landing sites.
            </div>
            <br> -->
            <div class="line"></div>
            <br>   
            <div class="flex justify-between">
                <div class="distance">
                    <div class="d-heading">
                        AVG. DISTANCE
                    </div>
                    <div class="d-data">
                        384,400 KM
                    </div>
                </div>
                <div class="travel-time">
                    <div class="d-heading">
                        EST. TRAVEL TIME
                    </div>
                    <div class="d-data">
                        3 DAYS
                    </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>
