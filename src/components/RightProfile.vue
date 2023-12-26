<script setup>
import BiographySection from './BiographySection.vue';
import ExperienceSection from './experiences/ExperienceSection.vue';
// import ProjectsSection from './projects/ProjectsSection.vue';
</script>

<template>
  <div class="right-profile">
    <biography-section />
    <br />
    <experience-section />
    <br />
    <!-- <projects-section /> -->
  </div>
</template>

<style scoped>
.right-profile {
  text-align: center;
}
</style>