<template>
    <section class="text-white mt-18" id="achievement">
        <div data-aos="flip-right" class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[100%]">
                <h2 class="text-4xl font-bold text-white text-left mb-4">
                    <span class="text-transparent bg-clip-text text-white">ACHIEVEMENTS</span>
                </h2> 
                <div class="space-y-8 py-8 font-mono" data-aos="fade-right">
                    <div v-for="item in Achievements" :key="item.id"
                    class="flex items-center rounded-xl p-4 bg-[#F1EFEC] shadow-lg border border-[#1f1641]"
                    >
                    <div class="w-1/4">
                        <img src="https://img.icons8.com/?size=100&id=LnEviQCbWLnq&format=png&color=000000" alt="lawyer">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ item.role }}
                        </h3>
                        <p class="text-black">{{ item.company }}</p>
                        <p class="text-black">{{ item.date }}</p>
                    </div>
                </div>
                </div>
            </div>
           <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[100%]">
                <h2 class="text-4xl font-bold text-white text-left mb-4">
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">SEMINAR ATTENDED</span>
                </h2> 
                <div class="space-y-8 py-8 font-mono" data-aos="fade-right">
                    <div v-for="item in Seminar" :key="item.id"
                    class="flex  items-center rounded-xl p-4 bg-[#F1EFEC] shadow-lg border border-[#1f1641]"
                    >
                    <div class="w-1/4">
                        <img src="https://img.icons8.com/?size=100&id=2QDhXdmrmfgU&format=png&color=000000" alt="lawyer">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">
                            {{ item.seminar }}
                        </h3>
                        <p class="text-black">{{ item.address }}</p>
                        <p class="text-black">{{ item.date }}</p>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
const Achievements =ref([
    {
        id:1,
        role:'Member ',
        company:'Computer Student’s Society',
        date:'2013-2014'
    },
    {
        id:2,
        role:'Certificate of Completion',
        company:'Alliance Near Hire Program',
        date:'2016-2017'
    },
    {
        id:3,
        role:'Certificate of Participation',
        company:'South GG Promotions Corp. Leadership Training',
        date: 'September 18, 2021'
    },
])
const Seminar =ref([
    {
        id:1,
        seminar:'GDG Campus Talk',
        address:'Case Room, Cebu Institute of Technology – University',
        date:'September 17,2016'
    },
    {
        id:2,
        seminar:'GDG Dev Fest Cebu 2016',
        address:'SM Seaside City Cebu',
        date:'November 19,2016'
    },
    {
        id:3,
        seminar:'Leadership Training',
        address:'Bayfront, Cebu City',
        date:'September 18, 2021'
    },
])
</script>