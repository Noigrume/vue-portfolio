<script setup>
defineProps(['id', 'title', 'description', 'image', 'languages'])
</script>

<template>
  <div class="article-card">
    <div class="article-image">
      <img :src="image" alt="Article Image" />
    </div>
    <div class="article-content">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>

      <p v-for="language in languages" :key="language.id">
        {{ language.text }}
      </p>

      <a href="{{link}}">Read More</a>
    </div>
  </div>
</template>

<style scoped>
.article-card {
  display: flex;
  margin: 10px;
  color: rgb(156, 156, 156);
  background-color: #181818e5;
}

.article-image {
  flex: 1;
  margin-right: 20px;
}

.article-image img {
  max-width: 100%;
  height: 100%;
}

.article-content {
  flex: 2;
}

.article-content h3 {
  font-size: 18px;
  margin: 0;
}

.article-content p {
  margin: 0;
}
</style>
