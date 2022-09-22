<script setup>
const route = useRoute();
const story = await useStoryblok(`project/${route.params.slug}`,{
    version: "draft",
});
</script>
<template>
  <StoryblokComponent v-if="story" :blok="story.content"></StoryblokComponent>
</template>
