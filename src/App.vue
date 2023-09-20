<script setup>
import { RouterView } from 'vue-router'
import NavBar from './components/Navbar.vue'
</script>

<template>
  <!-- <div id="app"> -->
  <NavBar />
  <router-view />
  <!-- </div> -->
</template>

<script>
export default {
  components: {
    NavBar
  }
}
</script>

<style></style>
