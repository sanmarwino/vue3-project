<template>
    <section class="text-white mt-18" id="skills">
        <div class="absolute right-0 top-[110rem] h-full w-full justify-end">
            <span class="flex opacity-20">
                <span class="w-16 h-32 rounded-l-full flex bg-primary blur-2xl"></span>
                <span class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"></span>
            </span>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[70%]">
                <h2 class="text-4xl font-bold text-white text-left mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">SKILLS</span>
                </h2>
                <div>
                    <div class="space-y-8 py-8" data-aos="fade-left">
                    <ul class="list-disc list-inside space-y-1 text-white text-lg font-mono">
                    <li>Javascript</li>
                    <li>Vue.js</li>
                    <li>Tailwindcss</li>
                    <li>HTML with CSS</li>
                    <li>Wordpress</li>
                    <li>PHP</li>
                    <li>NativeScript</li>
                    <li>Node.js</li>
                    <li>Spring MVC</li>
                    <li>Photoshop</li>
                    <li>XAMPP</li>
                    <li>PostgreSQL</li>
                    <li>MongoDB</li>
                    <li>Git Version Control</li>
                    </ul>
                    </div>
                </div>
            </div>
            <div data-aos="flip-left">
                <h2 class="text-4xl font-bold text-white text-left mb-8 md:text-center md:mt-0 mt-8 ">WORK EXPERIENCES</h2>
                <div class="space-y-8 py-8 font-mono" data-aos="fade-left">
                    <div v-for="element in Experinces" :key="element.id"
                    class="flex  items-center rounded-xl p-4 bg-[#F1EFEC] shadow-lg border border-[#1f1641]"
                    >
                    <div class="w-1/4">
                        <img src="https://img.icons8.com/?size=100&id=94482&format=png&color=000000" alt="lawyer">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ element.role }}
                        </h3>
                        <p class="text-black">{{ element.company }}</p>
                        <p class="text-black">{{ element.date }}</p>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
const Experinces =ref([
    {
        id:1,
        role:'Web Developer ',
        company:'South GG Promotions Corp. ',
        date:'November 27, 2018 – Feb 1, 2023'
    },
    {
        id:2,
        role:'Software Developer',
        company:'Wind’s Gate Philippine Software Development Inc. ',
        date:'March 2018 – September 2018'
    },
    {
        id:2,
        role:'Technical Support/ IT Staff',
        company:'(OJT 2) Oriental Port and Allied Services Corporation ',
    },
    {
        id:2,
        role:'Debugger  ',
        company:'(OJT 1) Cebu Institute of Technology University in CCS Department',
    },
])
</script>