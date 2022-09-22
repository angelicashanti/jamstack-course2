<script setup>
const story = await useStoryblok('home', {version: "draft",
resolve_relations: "featureProjects.projects"
})
</script>

<template>
  <StoryblokComponent v-if="story" :blok="story.content"></StoryblokComponent>
</template>
