<script setup>
import { ref } from 'vue';

import carditem from './items/carditem.vue';

const props = defineProps({
    title: String
})

const data = ref({
    genre: [
        {
            title: "action", preview: [
                "a", "b", "c"
            ]
        },
        {
            title: "racing", preview: [
                "a", "b", "c"
            ]
        },
        {
            title: "rpg", preview: [
                "a", "b", "c"
            ]
        },
        {
            title: "casual", preview: [
                "a", "b", "c"
            ]
        },
    ]
})
</script>

<template>
    <div class="text-white mx-5 my-3">
        <div class="d-flex w-100">
            <h4 class="me-auto" style="margin: 0px">{{ title }}</h4>
            <div class="d-flex justify-content-end btn-group">
                <button type="button" class="btn btn-outline-light">&laquo;</button>
                <button type="button" class="btn btn-outline-light">&raquo;</button>
            </div>
        </div>
        <hr>
        <div class="d-flex justify-content-center" style="gap: 2%">
            <carditem v-for="genre in data.genre" :title="genre.title" cardlg />
        </div>
    </div>
</template>