<template>
    <div class="grid grid-cols-12 gap-4 p-4">
        <Header />
        <Hero />
        <Project :projects="projects" />

        <div class="flex flex-wrap gap-4">
            <button type="button" 
            @click="isExperience = true"
            class="py-2.5 px-5 me-2 mb-2 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:ring-gray-100 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
            Experience
        </button>
            <button type="button" 
            @click="isExperience = false"
            class="py-2.5 px-5 me-2 mb-2 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-lg border border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:ring-gray-100 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
            Skills</button>

        </div>
        <div class="col-span-12">
            <div class="flex flex-wrap gap-4 justify-between">
                <Experience v-if="isExperience === true"/>
                <Skills v-else/>
            </div>
        </div>
    </div>
</template>

<script setup>
import Experience from '@/components/Experience.vue';
import Header from '@/components/Header.vue';
import Hero from '@/components/Hero.vue';
import Project from '@/components/Project.vue';
import Skills from '@/components/Skills.vue';
import { ref } from 'vue';

const isExperience = ref(true);

const projects = ref([
    {
        name: "Porfolio"
    },
    {
        name: "PeopleOps"
    },
    {
        name: "System Monitoring"
    },
     {
        name: "System Monitoring Solutions"
    }
])
</script>