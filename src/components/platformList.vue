<script setup>
import { ref } from 'vue';
import listitem from './items/listitem.vue';

const data = ref({
    platforms: [
        { title: "Nintendo Switch", icon: "bi bi-nintendo-switch" },
        { title: "Playstation", icon: "bi bi-playstation" },
        { title: "Steam", icon: "bi bi-steam" },
        { title: "Xbox", icon: "bi bi-xbox" }
    ]
})
</script>

<template>
    <listitem :datas="data.platforms" style="gap: 20%; color: white; height: 125px;" is-image />
</template>