<template>
  <div class="page about">
    <h1>A propos_</h1>

    <section>
      <p>
        > Conceptrice d'applications web de formation et après un an d'alternance chez Grand Est
        Automobile (PHP-LARAVEL/Back-end), je recherche un poste de développeuse dans les environs
        d'Aix-en-Provence. En parallèle je poursuis ma formation avec un diplôme d'ingénieur au CNAM
        "Architecture et intégration des systèmes et des logiciels" en cours du soir.
      </p>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.about {
  /* background-color: #fc6602; */
  background-color: rgb(23, 23, 23);
  display: flex;
  flex-direction: column;
  justify-content: left;
  align-items: top;
  min-height: 100vh;
}

section {
  border-left: #9f8d27 solid 2px;
  padding: 20px;
  margin: auto;
  color: rgb(182, 160, 22);
  text-shadow: 1px 1px 2px rgb(0, 0, 0);
  font-size: 1.4rem;
  max-width: 80%;
}

h1 {
  text-align: right;
  /* color: #fbe5b8; */
  color: rgb(233, 203, 10);
  margin: 0;
  padding: 20px;
  font-family: 'Oswald', sans-serif;
  font-size: 15rem;
  font-weight: bolder;
  font-style: italic;
  letter-spacing: 0.1rem;
}
</style>
