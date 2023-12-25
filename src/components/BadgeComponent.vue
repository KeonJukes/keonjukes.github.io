<script setup>
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
}

.badge-container:hover {
    background-color: #8dc931;
    color: white;
}
</style>