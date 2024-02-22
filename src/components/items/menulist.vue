<script setup>
const props = defineProps({
    menus: Array
})
</script>

<template>
    <nav id="navbar" class="navbar w-50">
        <ul class="d-flex justify-content-around w-100" style="list-style:none; margin: 0px;">
            <li v-for="menu in menus">
                <a href="#" class="nav-link">{{ menu }}</a>
            </li>
        </ul>
    </nav>
</template>