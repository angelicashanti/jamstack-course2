<script setup>
defineProps({
    blok: Object,
});
</script>
<template>
  <div class="container" v-editable="blok">
    <h1 style="margin-left: 10px">{{ blok.title }}</h1>
    <div class="featured-projects">
      <div class="projects" v-for="project in blok.projects" :key="project._uid" style="margin-right: 100px">
        <NuxtLink
          :to="{ name: 'project-slug', params: { slug: project.slug } }"
        >
          <img
            :src="project.content.image?.filename"
            :alt="project.content.image?.alt"
          />
          <h3>{{ project.content.name }}</h3>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
