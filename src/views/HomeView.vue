<script setup>
import SubTitle from '../components/SubTitle.vue'
</script>

<template>
  <header class="page home-page">
    <div id="main titles">
      <h1 id="portfolio-title">LUCIE SIMATOVIC</h1>
      <h2 id="portfolio-subtitle">> Developpeuse d'applications web</h2>
      <h2 id="portfolio-subtitle">> Laravel / PHP</h2>
    </div>
  </header>

  <SubTitle>
    <template #message> [ Bienvenue ! ] </template>
  </SubTitle>
</template>

<script>
export default {
  // Add any component-specific logic here
}
</script>

<style scoped>
#main-titles {
  display: flex;
  align-items: left;
  max-width: 650px;
}
#portfolio-title {
  font-family: 'Oswald', sans-serif;
  font-size: 10rem;
  font-weight: 900;
  letter-spacing: 0.1rem;
  /* color: #e5d48e; */
  color: rgb(255, 255, 255);
  /* text-shadow: 3px 3px 3px black; */
}
#portfolio-subtitle {
  color: rgb(255, 255, 255);
  font-size: 1.1rem;
  padding: 5px;
  margin: 0;
  text-align: left;
  background-color: rgba(0, 0, 0, 0.539);
  grid-column-start: 2;
}
.home-page {
  /* background-color: #00ad4a; */
  background: no-repeat url(@/assets/img/px.webp);
  background-size: cover;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
