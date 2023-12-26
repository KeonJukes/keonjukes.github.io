<script setup>
import { experiences } from './Experiences'
import ExperienceCard from './ExperienceCard.vue'

const experienceList = experiences
</script>

<template>
  <h2 class="experience-title">Experience</h2>
  <br />
  <div v-for="experience in experienceList" :key="experience.company">
    <span>
      <experience-card
        :company="experience.company"
        :title="experience.title"
        :description="experience.description"
        :start-date="experience.startDate"
        :end-date="experience.endDate"
        :experience-badges="experience.technologies"
      />
      <br />
    </span>
  </div>
</template>

<style scoped>
.experience-title {
  color: #8dc931;
}
</style>
