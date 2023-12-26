<script setup>
    import BadgeComponent from '../BadgeComponent.vue'

    defineProps({
        company: {
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
        startDate: {
            type: String,
            required: true
        },
        endDate: {
            type: String,
        },
        experienceBadges: {
            type: Array
        }
    })
</script>

<template>
<div class="card-container">
    <div class="date-section">
        <span>
            <p>{{ `${startDate} -  ${endDate ?? 'present'}` }}</p>
        </span>
    </div>
    <div class="main-card">
        <h2 class="experience-company">{{ company }}</h2>
        <h3 class="experience-title">{{ title }}</h3>
        <p class="experience-description">{{ description }}</p>
        <div class="experience-badges-container">
            <span v-for="badge in experienceBadges" :key="badge.name">
            <badge-component :badge="badge"/>
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

.date-section {
    height: auto;
    width: 65%;
    text-align: start;
    opacity: 70%;
}

.main-card {
    height: auto;
    width: 80%;
    text-align: start;
}

.experience-company {
    font-weight: 700;
}

.experience-title {
    font-weight: 600;
    color: #8dc931
}

.experience-description {
    margin-bottom: 10px;
}

.experience-badges-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}
</style>