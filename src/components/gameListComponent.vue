<script setup>
import { ref } from 'vue';
import carditem from './items/carditem.vue';

const props = defineProps({
    title: String,
})

const data = ref({
    gameList: [
        { title: "Dying Light", img: "./src/assets/images/dl.jpg" },
        { title: "Assassin's Creed", img: "./src/assets/images/ac4.jpg" },
        { title: "Zelda", img: "./src/assets/images/botw.jpg" },
        { title: "Grand Thef Auto", img: "./src/assets/images/gta5.png" },
        { title: "Skyrim", img: "./src/assets/images/skyrim.png" },
        { title: "Spider Man", img: "./src/assets/images/sm.jpg" },
    ],

    game: [
        {
            arr: [
                {}, {}
            ]
        },

        {
            arr: [
                {}, {}
            ]
        },

        {
            arr: [
                {}, {}
            ]
        }
    ]
})
</script>

<template>
    <div class="text-white ms-5 me-5">
        <div class="d-flex w-100">
            <h4 class="me-auto" style="margin: 0px;">{{ title }}</h4>
            <div class="d-flex justify-content-end btn-group" role="group">
                <button type="button" class="btn btn-outline-light">&laquo;</button>
                <button type="button" class="btn btn-outline-light">&raquo;</button>
            </div>
        </div>
        <hr>
        <div class="d-flex w-100 justify-content-center" style="gap: 2%;">
            <carditem v-for="game in data.gameList" :title="game.title" :img="game.img" />
        </div>
    </div>
</template>