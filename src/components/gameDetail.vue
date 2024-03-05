<script setup>
const props = defineProps({
    title: String,
    mainImage: String,
    coverImage: String,
    desc: String,
})
</script>

<template>
    <div class="bg-dark">
        <div class="head">
            <div class="black-box"></div>
            <img :src="mainImage" alt="image" class="main-image">
            <img :src="coverImage" alt="image" class="cover-image">
        </div>
        <div class="main">
            <h5>{{ title }}</h5>
            <p>{{ desc }}</p>
        </div>
    </div>
</template>