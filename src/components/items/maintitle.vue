<script setup>
const props = defineProps(["value"])
</script>

<template>
    <h3 class="me-auto" style="margin: 0px;">
        <a href="#" class="link-underline link-underline-opacity-0 link-light">{{ value }}</a>
    </h3>
</template>