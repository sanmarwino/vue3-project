<template >
    <section class="text-white mt-20" id="about">
        <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
            <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"></div>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white text-left mb-8">EDUCATION</h2>
                <div class="space-y-8 py-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w-[80%] w-full rounded-xl bg-[#F1EFEC] shadow-lg border border-[#1f1641]"
                    >
                        <div class="w-1/4 justify-items-center">
                            <img src="https://img.icons8.com/?size=100&id=12197&format=png&color=000000" alt="graduation-cap--v1">
                        </div>
                        <div class="w-3/4 pl-4 font-mono">
                            <h3 class="text-2xl text-transparent bg-clip-text bg-gradient-to-r from-primary to-gray-500 lg:text-xl">
                                {{ element.School }}
                            </h3>
                            <p class="text-black">{{ element.program }}</p>
                             <p class="text-black">{{ element.program1 }}</p>
                            <p class="text-black">{{ element.address }}</p>
                            <p class="text-black">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">PROFILE</span>
                </h2>
                  <div>
                    <div class="flex items-end justify-between" data-aos="fade-right">
                    <ul class="space-y-8 text-lg pt-10">
                    <li class="text-white font-mono"><span class="font-bold uppercase">Fullname:</span> Marwin Joseph Medado</li>
                    <li class="text-white font-mono"><span class="font-bold uppercase">Birth Date:</span> February 13, 1996</li>
                    <li class="text-white font-mono"><span class="font-bold uppercase">Job:</span> Freelancer, Frontend Developer</li>
                    <li class="text-white font-mono"><span class="font-bold uppercase">Contact # :</span> +63 9052633768</li>
                    <li class="text-white font-mono"><span class="font-bold uppercase">Email:</span> marwinmedado@gmail.com</li>
                    </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
const education=ref([
    {
        id:1,
        School:'Cebu Institute of Technology – University',
        program:'Bachelor of Science in Information Technology',
        program1:'Tertiary Level',
        address:'N. Bacalso Avenue, Cebu City ',
        year:'2013-2017'
    },
    {
        id:2,
        School:'Salazar Colleges of Science and Institute of Technology',
        program:'Secondary Level',
        address:'N.Bacalso Avenue, Cebu City',
        year:'2009-2013'
    },
    {
        id:3,
        School:'Tisa 1, Elementary School',
        program:'Elementary Level',
        address:'Tisa, Cebu City',
        year:'2003-2009'
    }
])
</script>