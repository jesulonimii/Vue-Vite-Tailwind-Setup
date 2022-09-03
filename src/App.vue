<template>


  <main class="text-white flex bg-slate-800 relative">
    <SideBar class="z-50 h-screen fixed" @collapsed="resizeView"/>
    <RouterView id="view" class="ml-[250px] transition-all duration-1000" />

  </main>


</template>

<script setup>
import {RouterLink, RouterView} from 'vue-router'
import SideBar from './components/SideBar.vue'


function resizeView(state) {
  const view = document.querySelector('#view')
  console.log("state", state)

  if (state) {
    view.setAttribute("style", "margin-left: 100px")
  } else {
    view.setAttribute("style", "margin-left: 250px")

  }


}
</script>


