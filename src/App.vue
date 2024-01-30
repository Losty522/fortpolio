<script setup>
import MainCard from './components/MainCard.vue';
import ProjectCard from './components/ProjectCard.vue';
import Navbar from './components/Navbar.vue'
import Contanct from './components/Contanct.vue';
import NavbarFooter from './components/NavbarFooter.vue';
</script>

<template>
  
  <Navbar />
  <MainCard />
  <ProjectCard />
  <Contanct />
  <NavbarFooter />
  <div class="gradient-background"></div>
</template>

<style >

.gradient-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to right, #a1f0db, #91df86); /* グラデーションの色を指定 */
  animation: moveGradient 2s linear infinite; /* 適宜調整 */
  z-index: -1;
}
@keyframes moveGradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
</style>
