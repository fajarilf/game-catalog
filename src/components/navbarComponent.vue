<script setup>
import { ref } from "vue"
import mainTitle from "./items/maintitle.vue"
import menuList from "./items/menulist.vue"

const props = defineProps(["title"])

const menus = ref(["Home", "About", "Genre", "Platform"])

</script>

<template>
    <div class="container d-flex align-items-center p-3">
        <mainTitle :value="props.title" />
        <menuList :menus="menus" />
    </div>
</template>