<template>
    <div class="grid grid-cols-12 gap-4 p-4">
        
        <Header/>
        <Hero/>
        <Project/>

        <!-- Experience -->
        <div class="col-span-12">
                        <div class="flex flex-wrap gap-4 justify-between">
                            <div class="border rounded h-[500px] w-[49%]">Experience</div>
                            <div class="border rounded h-[500px] w-[49%]">Skills</div>
                        </div>

            </div>
    </div>
</template>

<script setup>
import Header from '@/components/Header.vue';
import Hero from '@/components/Hero.vue';
import Project from '@/components/Project.vue';
</script>