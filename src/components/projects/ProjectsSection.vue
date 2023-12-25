<script setup>
import ProjectCard from './ProjectCard.vue';
import { projects } from './Projects';

const projectList = projects
</script>

<template>
  <div>
    <h3 class="projects-title">Projects</h3>
    <br />
    <div v-for="project in projectList" :key="project.title">
      <project-card :title="project.title" :photo="project.photo" :description="project.description" :project-badges="project.technologies"/>
      <br />
    </div>
  </div>

</template>

<style scoped>
.projects-title {
    color: #8dc931
}
</style>