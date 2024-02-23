<script setup>
import { ref } from 'vue';
import carouselitem from './items/carouselitem.vue';

const carouselData = ref([
    { id: 1, img: "./src/assets/images/re4.jpg", title: "First", desc: "first item" },
    { id: 2, img: "./src/assets/images/gow.jpg", title: "Second", desc: "second item" },
    { id: 3, img: "./src/assets/images/dg.jpg", title: "Third", desc: "third item" }
])
</script>

<template>
    <div id="carousel" class="carousel slide carousel-fade" data-bs-ride="carousel">
        <div class="carousel-indicators">
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="0" class="active" aria-current="true"
                aria-label="Slide 1"></button>
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
            <button type="button" data-bs-target="#carousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
        </div>
        <div class="carousel-inner">
            <carouselitem :datas="carouselData" />
        </div>
    </div>
</template>