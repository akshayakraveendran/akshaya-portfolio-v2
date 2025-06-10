<template>
  <div class="col-span-12">
            <div class="flex flex-wrap gap-4 justify-between">
                <template v-for="(project, index) in projects" :key="index">
                    <div class="border rounded h-[200px] w-[30%]">{{ project.name }}</div>
                </template>
            
            </div>
        </div>
</template>

<script setup>
import { onBeforeMount, onMounted, onUpdated } from 'vue';


defineProps({
    projects: {
        type: Array,
        default: [],
        required: true
    }
});




onBeforeMount(()=>{
    console.log('>> Before Mount',)
})

onMounted(()=>{
    console.log('>> mounted')
})

onUpdated(()=>{
    console.log('>> updated')
})
</script>