<script setup>
import { computed, ref } from 'vue';

const props = defineProps({
    datas: Array,
})

const activeClass = (id) => {
    if (id === "1") return "active"
}

</script>

<template>
    <div class="carousel-item" v-for="data in datas" :class="activeClass(String(data.id))">
        <div class="d-flex justify-content-center">
            <div class="black-box"></div>
            <img :src="data.img" alt="item" class="d-block img-fluid w-75">
        </div>
        <div class="carousel-caption d-none d-md-block">
            <h5>{{ data.title }}</h5>
            <p>{{ data.desc }}</p>
        </div>
    </div>
</template>

<style>
.black-box {
    height: 100%;
    width: 100%;
    background: rgb(0, 0, 0);
    background: linear-gradient(90deg, rgba(0, 0, 0, 1) 13%, rgba(255, 255, 255, 0) 50%, rgba(0, 0, 0, 1) 87%);
    position: absolute;
}
</style>