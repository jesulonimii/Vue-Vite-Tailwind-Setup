<template>


  <main class="text-white flex bg-slate-800 h-screen">
    <SideBar class="z-50"/>
    <RouterView />

  </main>


</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import SideBar from './components/SideBar.vue'

</script>


