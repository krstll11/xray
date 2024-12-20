<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Footer from './components/Footer.vue';
import { RouterView } from 'vue-router';
</script>

<template>
  <div>
    <HelloWorld></HelloWorld> 
    <RouterView></RouterView>
    <Footer></Footer>
  </div>
</template>

<style scoped>

</style>
