<script setup>
import BadgeComponent from '../BadgeComponent.vue';

    defineProps({
        photo: {
            type: String,
            required: true
        },
        title: {
            type: String,
            required: true
        },
        description: {
            type: String,
            required: true
        },
        projectBadges: {
            type: Array
        }
    })
</script>

<template>
<div class="card-container">
    <div class="photo-section">
    <img :src="photo"/>
    </div>
    <div class="main-card">
        <h2 class="project-title">{{ title }}</h2>
        <p class="project-description">{{ description }}</p>
        <div class="project-badges-container">
            <span v-for="badge in projectBadges" :key="badge">
            <badge-component :badge-title="badge"/>
            </span>
        </div>
    </div>
</div>
</template>

<style scoped>
.card-container {
    display: flex;
    width: auto;
    height: auto;
}

.main-card {
    height: auto;
    text-align: start;
}

.photo-section {
    margin-right: 22px;
}

.project-badges-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}

.project-title {
    font-weight: 700;
}

.project-description {
    margin-bottom: 10px;
}
</style>