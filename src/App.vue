<template>


  <main class="text-white flex bg-slate-800">
    <SideBar/>
    <div class="flex flex-col w-full h-full h-screen">
      <div class="px-10 pt-10 pb-5 text-white font-bold text-3xl capitalize">{{ this.$route.name }}</div>
      <RouterView class="flex-grow" />
    </div>
  </main>


</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import SideBar from './components/SideBar.vue'

</script>


