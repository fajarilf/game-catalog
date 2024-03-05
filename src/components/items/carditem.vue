<script setup>
const props = defineProps({
    title: String,
    img: String
})
</script>

<template>
    <div>
        <div class="c-card">
            <RouterLink to="/">
                <img :src="img" alt="image" class="w-100 h-100 border border-dark border-2 rounded object-fit-cover">
            </RouterLink>
        </div>
        <div class="title text-center">
            <h5>{{ title }}</h5>
        </div>
    </div>
</template>

<style scoped>
.c-card {
    height: 12rem;
    width: 10rem;
}

.c-card:hover {
    -webkit-mask-image: linear-gradient(black, transparent);
    mask-image: linear-gradient(black, transparent);
}
</style>