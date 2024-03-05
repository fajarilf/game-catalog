<script setup>
const props = defineProps({
    datas: Array,
    isImage: Boolean,
})

const textOnly = (data) => {
    if (!props.isImage) return data
}

</script>

<template>
    <ul class="d-flex w-100 justify-content-center align-items-center" style="list-style:none; margin: 0px;"
        :style="$attrs.style">
        <li v-for="data in datas">
            <a href="#" class="nav-link">
                <div v-if="isImage" class="text-center">
                    <i :class="data.icon"></i>
                </div>

                {{ textOnly(data) }}
            </a>
            <!-- <div v-else class="text-center">
                <i :class="data.icon" class="fs-1"></i>
                <p>{{ data.title }}</p>
            </div> -->
        </li>
    </ul>
</template>

<style scoped>
li {
    font-size: 2.5em;
    transition: 0.2s ease-in;
}

li:hover {
    font-size: 2.8em;
}

ul {
    padding-inline-start: 0;
}
</style>