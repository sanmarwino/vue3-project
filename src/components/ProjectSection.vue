<template>
    <section class="text-white mt-20" id="projects">
        <div class="px-4 xl:pl-16">
            <div class="mb-4 md:flex md:justify-between xl:pr-16">
                <h2 class="text-4xl font-bold text-white"> PROJECTS</h2>
                <div class="flex space-x-4 mb-4 mt-5 md:mt-0 text-2xl font-momo">
                    <!-- <button class="hover:text-primary  rounded-full bg-secondary px-5 font-momo text-black" v-for="category in ['ALL', 'WEB DEVELOPMENT', 'MOBILE APP']"
                        :key="category" @click="() => selectedCategory = category">
                        {{ category }}
                    </button> -->
                </div>
            </div>
            <ul class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3"
                data-aos="fade-right">
                <div v-for="project in filteredProjects" :key="project.id">
                    <div class="h-52 md:h-[24rem] rounded-t-xl relative group bg-[center_top_1rem]"
                    :style="{ backgroundImage: 'url(' + project.image + ')', backgroundSize: 'cover'  }">                    
                    <div class="overlay items-center justify-center absolute top-0 left-0 w-full h-full bg-[#181818] bg-opacity-0
                    hidden group-hover:flex group-hover:bg-opacity-80 transition-all duration-500
                    ">
                        <a class="h-14 w-14 mr-2 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
                            :href="project.webURL"> <svg xmlns="http://www.w3.org/2000/svg" fill="none"
                                viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true"
                                data-slot="icon"
                                class="h-10 w-10 text-[#ADB7BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2  cursor-pointer group-hover/link:text-white">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M2.036 12.322a1.012 1.012 0 0 1 0-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178Z">
                                </path>
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"></path>
                            </svg></a>
                            <!-- <a
                            class="h-14 w-14 border-2 relative rounded-full border-[#ADB7BE] hover:border-white group/link"
                            :href="project.gitURL"> <svg xmlns="http://www.w3.org/2000/svg" fill="none"
                                viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true"
                                data-slot="icon"
                                class="h-10 w-10 text-[#ADB7BE] absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2  cursor-pointer group-hover/link:text-white">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M2.036 12.322a1.012 1.012 0 0 1 0-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178Z">
                                </path>
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z"></path>
                            </svg></a> -->
                    </div>
                </div>
                <div class="text-white rounded-b-xl mt-3 bg-[#F1EFEC] shadow-lg border border-[#1f1641] py-6 px-4 ">
                    <h3 class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary text-2xl"> {{ project.title }}</h3>
                    <p class="text-black h-1/2">{{ project.description }}</p>
                    <div class="flex flex-wrap p-2.5">
                        <div v-for="technology in project.technologies" :key="technology" class="text-center ml-1 mt-1 rounded-3xl px-3 bg-[#111827]"
                        style="box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1); border: 1px solid #111827;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);"
                        >
                    <p class="px-1 py-2">{{ technology }}</p>
                    </div>
                    </div>
                </div>
                </div>
            </ul>
        </div>
    </section>
</template>
<script setup>
import { ref, computed } from 'vue';

const Projects = ref([
    {
        id: 1,
        category: 'web development',
        image: './zealsgg.jpg',
        title: 'Zeals Esports',
        description: 'Zeal Esports is a Filipino esports organization, known for its involvement in the VALORANT scene, and has a history of competing in major tournaments like VCT Stage 1. ',
        technologies: ['Wordpress'],
        gitURL: '',
        webURL: 'https://www.zeals.gg/about/'
    },
    {
        id: 2,
        category: 'web development',
        image: './foresight.jpg',
        title: 'Foresight.ph',
        description: 'Esports website',
        technologies: ['Vue.js 2', 'Vuetify 2', 'Node.js', 'Xampp',],
        gitURL: '',
        webURL: 'https://foresight.ph/'
    },
    // {
    //     id: 3,
    //     category: 'web development',
    //     image: 'src/assets/project.png',
    //     title: 'project 1',
    //     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic tenetur quasi ipsam labore sapiente, accusamus necessitatibus laboriosam non voluptas inventore deserunt dolore modi ex, praesentium at provident nihil magni ratione!',
    //     technologies: ['vue.js 3', 'vuex', 'Express'],
    //     gitURL: '',
    //     webURL: ''
    // },
    // {
    //     id: 4,
    //     category: 'Mobile App',
    //     image: 'src/assets/mobile.jpg',
    //     title: 'project 1',
    //     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic tenetur quasi ipsam labore sapiente, accusamus necessitatibus laboriosam non voluptas inventore deserunt dolore modi ex, praesentium at provident nihil magni ratione!',
    //     technologies: ['vue.js 3', 'vuex', 'Express'],
    //     gitURL: '',
    //     webURL: ''
    // },
    // {
    //     id: 5,
    //     category: 'web development',
    //     image: 'src/assets/project.png',
    //     title: 'project 1',
    //     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic tenetur quasi ipsam labore sapiente, accusamus necessitatibus laboriosam non voluptas inventore deserunt dolore modi ex, praesentium at provident nihil magni ratione!',
    //     technologies: ['vue.js 3', 'vuex', 'Express'],
    //     gitURL: '',
    //     webURL: ''
    // },
    // {
    //     id: 6,
    //     category: 'Mobile App',
    //     image: 'src/assets/mobile.jpg',
    //     title: 'project 1',
    //     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic tenetur quasi ipsam labore sapiente, accusamus necessitatibus laboriosam non voluptas inventore deserunt dolore modi ex, praesentium at provident nihil magni ratione!',
    //     technologies: ['vue.js 3', 'vuex', 'Express'],
    //     gitURL: '',
    //     webURL: ''
    // }
]);

const selectedCategory = ref('ALL');
const filteredProjects = computed(() => {
    if (selectedCategory.value === 'ALL') {
        return Projects.value;
    }
    return Projects.value.filter(project => project.category.toLocaleLowerCase() === selectedCategory.value.toLocaleLowerCase());
})

</script>