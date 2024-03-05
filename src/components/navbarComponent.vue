<script setup>
import { onMounted, onUnmounted, ref } from "vue";
import mainTitle from "./items/maintitle.vue"
import menuList from "./items/menulist.vue"

const props = defineProps({
    title: String,
    bgColor: String
})

const data = ref({
    bgColor: "",
})

window.addEventListener("scroll", (event) => {
    var top = window.scrollY

    data.value.bgColor = top > 5 ? "blurred" : ""

    event.preventDefault()
})

</script>

<template>
    <div class="d-flex align-items-center py-3 fixed-top" :class="data.bgColor"
        style="padding-left: 10%; padding-right: 10%;">
        <mainTitle :value="props.title" />
        <menuList class="justify-content-end" style="gap: 10%;" />
    </div>
</template>

<style scoped>
.blurred {
    backdrop-filter: blur(10px);
}
</style>