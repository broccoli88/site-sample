<template>
    <div class="tile">
        <span class="tile-description"> {{ gallery.theme }}</span>
        <img class="tile-img" :src="gallery.path" alt="japan" />
    </div>
</template>
<script setup>
import { ref } from "vue";

const props = defineProps(["gallery"]);
</script>
<style scoped>
.tile {
    position: relative;
}

.tile-description {
    display: none;
    justify-content: center;
    align-items: center;

    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 1;

    text-transform: uppercase;
    color: white;
    font-weight: 900;
    font-size: clamp(2rem, 2.8vw, 3.5rem);

    background-color: var(--color-accent-hover);
}

.tile:hover .tile-description {
    display: flex;
}
.tile-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>
