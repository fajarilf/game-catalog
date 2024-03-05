<script setup>
import { inject } from 'vue';

// const props = defineProps({
//     menus: Array,
// })

const value = inject("id");

</script>

<template>
    <nav id="navbar" class="navbar w-50">
        <ul class="d-flex w-100" :class="$attrs.class" style="list-style:none; margin: 0px;" :style="$attrs.style">
            <li v-for="menu in value">
                <a :href="menu.id"
                    class="link-underline link-underline-opacity-0 link-opacity-75 link-opacity-100-hover link-light">{{
            menu.title }}</a>
            </li>
        </ul>
    </nav>
</template>