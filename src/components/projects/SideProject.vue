<template>
  <div class="project-table">
    <table>
      <thead>
        <tr>
          <th></th>
          <th>Description</th>
          <th>Language</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="project in projects" :key="project.id">
          <td>{{ project.name }}</td>
          <td class="side-project-description">{{ project.description }}</td>
          <td class="prog-langage">{{ project.language }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          name: 'Project 1',
          description: 'je sais plus',
          language: 'JavaScript',
        },

        {
          id: 2,
          name: 'Project 1',
          description: 'Générateur d\'avatar',
          language: 'PHP',
        },

        {
          id: 3,
          name: 'Project 1',
          description: 'Aventure textuelle',
          language: 'javascript',
        },
        {
          id: 3,
          name: 'Project 1',
          description: 'Site e-commerce symfony',
          language: 'symfony',
        },

        {
          id: 3,
          name: 'Project 1',
          description: 'Site vitrine salon de thé from scratch',
          language: 'php',
        },
   
      ],
    };
  },
};
</script>

<style scoped>
table{
  color: rgb(190, 190, 190);
  margin: 0;
}
td{
  margin-top: 20px;
}

.side-project-description{
  font-style: italic;
  text-decoration: underline rgba(255, 255, 255, 0.178);
}
.prog-langage{
  background-color: rgb(67, 44, 150);
  border-radius: 5%;
  padding: 0;
  color:rgb(190, 190, 190);
}
</style>


