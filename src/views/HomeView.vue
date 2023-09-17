<script setup>
import SubTitle from '../components/SubTitle.vue'
</script>

<template>
  <div class="page home-page">
    <h1 id="portfolio-title">LUCIE SIMATOVIC</h1>
    <h2 id="portfolio-subtitle">> Developpeuse d'applications web</h2>
    <h2 id="portfolio-subtitle">> Laravel / PHP</h2>
  </div>

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
#portfolio-title {
  word-break: break-word;
  /* font-family: 'Oswald', sans-serif; */
  max-width: 800px;
  font-family: 'Darumadrop One', cursive;
  font-size: 8rem;
  /* color: #e5d48e; */
  color: rgb(192, 3, 3);
  text-shadow: 3px 3px 3px black;
  font-weight: bolder;
  line-height: 1;
}
#portfolio-subtitle {
  color: rgb(0, 0, 0);
  font-weight: bolder;
  font-size: 1.5rem;
  padding: 5px;
  text-align: left;
  background-color: rgba(255, 255, 255, 0);
}
.home-page {
  /* background-color: #00ad4a; */
  background: no-repeat url(@/assets/img/px.webp);
  background-size: cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

@-webkit-keyframes slidein {
  from {
    background-position: top;
    background-size: contain;
  }
  to {
    background-position: -100px 0px;
    background-size: contain;
  }
}

@keyframes slidein {
  from {
    background-position: top;
    background-size: contain;
  }
  to {
    background-position: -100px 0px;
    background-size: contain;
  }
}
/* Add additional styles as needed */
</style>
