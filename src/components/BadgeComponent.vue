<script setup>
import { badges } from '../badges'

defineProps({
  badgeTitle: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="badge-container">
    {{ badgeTitle }}
    <span class="tooltiptext">{{ badges[badgeTitle]['description'] }}</span>
  </div>
</template>

<style scoped>
.badge-container {
  height: 25px;
  width: 100px;
  border-radius: 30px;
  background-color: purple;
  text-align: center;
  margin: 2px;
  color: white;
  position: relative;
  display: inline-block;
}

.badge-container:hover {
  background-color: #8dc931;
  color: white;
}

.badge-container .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;

  /* Position the tooltip text */
  position: absolute;
  z-index: 1;
  bottom: 100%;
  left: 50%;
  margin-left: -60px;
}

.badge-container .tooltiptext::after {
  content: ' ';
  position: absolute;
  top: 100%; /* At the bottom of the tooltip */
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: black transparent transparent transparent;
}

.badge-container:hover .tooltiptext {
  visibility: visible;
}
</style>
