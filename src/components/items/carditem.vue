<script setup>
import { computed, onMounted, ref } from 'vue';

const props = defineProps({
    title: String,
    img: [String, Array],
    cardlg: {
        type: Boolean,
        default: false
    }
})

const cardSize = ref("")

onMounted(() => {
    cardSize.value = props.cardlg === true ? "c-card-lg bg-dark" : "c-card-sm"
})

</script>

<template>
    <div>
        <div :class="cardSize">
            <RouterLink to="/">
                <img v-if="!cardlg" :src="img" alt="image"
                    class="w-100 h-100 border border-dark border-2 rounded object-fit-cover">
                <div v-else class="d-flex justify-content-center">
                    <div class="c-card-inner border border-dark border-0 rounded bg-secondary"></div>
                    <div class="c-card-inner border border-dark border-0 rounded bg-white position-absolute">
                    </div>
                    <div class="c-card-inner border border-dark border-0 rounded bg-secondary"></div>
                </div>
            </RouterLink>
        </div>
        <div class="title text-center">
            <h5>{{ title }}</h5>
        </div>
    </div>
</template>

<style scoped>
.c-card-sm {
    height: 12rem;
    width: 10rem;
}

.c-card-lg {
    height: 12rem;
    width: 15rem;
    display: flex;
    justify-content: center;
    align-items: center;
    border: none;
    border-radius: 5px;
}

.c-card-inner {
    height: 9rem;
    width: 7rem;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.c-card-sm:hover,
.c-card-lg:hover {
    -webkit-mask-image: linear-gradient(black, transparent);
    mask-image: linear-gradient(black, transparent);
}
</style>