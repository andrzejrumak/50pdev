<script setup>
import { reactive } from 'vue'

const { data } = await useAsyncData('modules', () => $fetch('/api/modules'));
const modules = reactive(data.value)
</script>
<template>
<div>
  <div class="max-w-md mx-auto bg-white rounded-xl shadow-md overflow-hidden md:max-w-2xl mb-3">
    <div class="md:flex">
      <div class="md:flex-shrink-0">
        <img class="h-48 w-full object-cover md:h-full md:w-48" src="/nuxt.png" alt="Nuxt logo">
      </div>
      <div class="p-8">
        <div class="uppercase tracking-wide text-sm text-green-500 font-semibold">Nuxt 3 beta</div>
        <a href="#" class="block mt-1 text-lg leading-tight font-medium text-black hover:underline">It is time to anounce!!!</a>
        <p class="mt-2 text-green-900">Finaly Nuxt 3 beta public is alive. Let's check the future of frontend development.</p>
      </div>
    </div>
  </div>
  <div class="max-w-md mx-auto bg-white rounded-sm shadow-md overflow-hidden md:max-w-6xl my-4 ">
    <div class="border-green-900 border-2 ">
      <div class="text-2xl text-green-900 m-3">
        What Nuxt 3 modules are ready
      </div>
      <div class="m-3 md:grid grid-cols-2">
        <div v-for="module in modules" :key="module.name"> 
          <div class="text-emerald-600 border-2 border-emerald-700 m-3 ">        
            <p class="text-center m-2 text-lg text-green-900">Module name: {{ module.name }}</p>
            <div class="md:grid grid-cols-2">
              <p>Bridge module status: {{ module.bridge }}</p>
              <p>Core module status: {{ module.core}}</p>
              <a :href="module.repoUrl" v-if="module.repoUrl"><p class="text-left ml-2">Module repository</p> </a>
              <a :href="module.issueUrl" v-if="module.issueUrl"><p class="text-left ml-2">Module issue</p> </a>
            </div>
            <p class="text-center m-2">Module creator: {{ module.maintainers}}</p>
          </div>
        </div> 
      </div>
    </div>
  </div>
</div>
</template>

