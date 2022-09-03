<template>

  <div id="bar" style="width: 200px" class="h-screen bg-slate-800 p-8 justify-between transition-[width] duration-1000 overflow-hidden">

    <div class="h-fit w-fit flex">
      <i id="toggle" class="w-full h-full uil uil-angle-double-left origin-center transition duration-1000 cursor-pointer mx-2 text-3xl w-full" @click="sideBar"></i>
    </div>

    <div class="h-[80%] flex flex-col">

      <SideBarItem icon="estate" name="Home" link="/home" class="active" />
      <SideBarItem icon="user" name="Profile" link="/home" />
      <SideBarItem icon="setting" name="settings" link="/home" />
      <SideBarItem icon="history" name="History" link="/home" />
      <SideBarItem icon="search" name="Search" link="/home" />

    </div>

    <div class="h-[10%]">
      <SideBarItem icon="signout" name="Logout" link="/logout" />
    </div>
    
  </div>
  
</template>

<script setup>
import SideBarItem from './SideBarItem.vue'

function sideBar() {
  const bar = document.querySelector('#bar')
  const label = document.querySelectorAll('#label')
  const toggle = document.querySelector('#toggle')

  if (bar.getAttribute('style') === 'width: 200px;') {

    bar.setAttribute("style", "width: 100px;")
    toggle.setAttribute("style", "transform: rotate(180deg)")

    label.forEach(x=> {
      x.setAttribute("style", "opacity: 0;")
    })

  }
  else {
    bar.setAttribute("style", "width: 200px;")
    toggle.setAttribute("style", "transform: rotate(0deg)")


    label.forEach(x=> {
      x.setAttribute("style", "opacity: 1;")
    })
  }
}

</script>

<style scoped>
.active{
  color: #fbbf24;
}
</style>
