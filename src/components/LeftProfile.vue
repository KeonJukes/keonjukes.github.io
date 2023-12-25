<script setup>
import BiographySection from './BiographySection.vue';
import ExperienceSection from './experiences/ExperienceSection.vue';
// import ProjectsSection from './projects/ProjectsSection.vue';
</script>

<template>
  <div class="left-profile">
    <biography-section />
    <br />
    <experience-section />
    <br />
    <!-- <projects-section /> -->
  </div>
</template>

<style scoped>
.left-profile {
  height: 100vh;
  text-align: center;
}
</style>