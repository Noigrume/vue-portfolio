<script setup>
import { ref } from 'vue'
import ArticleCard from '../components/projects/MainProject.vue'

const projects = ref([
  {
    id: 1,
    title: 'Portfolio',
    description: 'Mon portfolio personnel réalisé avec Vue 3.',
    image: 'https://picsum.photos/200/200',
    languages: [
      { id: 1, text: 'Item 3' },
      { id: 2, text: 'Item 4' }
    ]
  },
  {
    id: 2,
    title: 'API Laravel ',
    description: 'Another example of an article card.',
    image: 'https://picsum.photos/200/200',
    languages: [
      { id: 1, text: 'Item 5' },
      { id: 2, text: 'Item 6' }
    ]
  },
  {
    id: 3,
    title: 'Sample Article 3',
    description: 'Another example of an article card.',
    image: 'https://picsum.photos/200/200',
    languages: [
      { id: 1, text: 'Item 1' },
      { id: 2, text: 'Item 2' }
    ]
  }
])
</script>

<template>
  <div class="page projects">
    <h1>Projets_</h1>
    <main class="container">
      <p class="project-section-description">> Projets principaux en cours de développement</p>

      <div class="article-wall">
        <ArticleCard
          v-for="project in projects"
          :key="project.id"
          :title="project.title"
          :image="project.image"
          :languages="project.languages"
          :description="project.description"
        >
        </ArticleCard>
      </div>

      <p class="project-section-description">
        > Tous les projets abandonnés, réalisés en cours ou suivant des tutos
      </p>

      <project-table />
    </main>
  </div>
</template>

<script>
import ProjectTable from '../components/projects/SideProject.vue'

export default {
  components: {
    ProjectTable
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: space-around; /* Horizontally */
  align-items: left;
  align-content: space-around;
}

h1 {
  background-color: #332c75;
  width: 100%;
  color: #8277e0;
  text-align: center;
  margin: 0;
  font-family: 'Oswald', sans-serif;
  font-size: 10rem;
  font-weight: bolder;
  font-style: italic;
  letter-spacing: 0.1rem;
}
.projects {
  background-color: rgb(37, 37, 37);
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  color: aliceblue;
  justify-content: center; /* Horizontally */
}
.project-section-description {
  display: flex;
  flex-direction: row;
  border-left: 1px solid white;
  padding: 15px;
  width: 100%;
}

.article-wall {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
</style>
