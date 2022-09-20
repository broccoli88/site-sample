<template>
    <div class="wrapper">
        <section class="photo-sessions">
            <GalleryTile
                v-for="gallery in galleryThemes"
                :key="gallery.theme"
                :gallery="gallery"
            />
        </section>
    </div>
</template>

<script setup>
import { reactive } from "vue";
import GalleryTile from "../reusable/GalleryTile.vue";

const galleryThemes = reactive([
    {
        theme: "japan",
        path: "https://images.unsplash.com/photo-1545569341-9eb8b30979d9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2670&q=80",
    },
    {
        theme: "estonia",
        path: "https://images.unsplash.com/photo-1567499128215-278710957d55?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2747&q=80",
    },
    {
        theme: "spain",
        path: "https://images.unsplash.com/photo-1543783207-ec64e4d95325?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2670&q=80",
    },
    {
        theme: "hawaii",
        path: "https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2673&q=80",
    },
]);
</script>

<style scoped>
.photo-sessions {
    display: grid;
    grid-template-columns: auto;
    gap: 8px;
}
@media (min-width: 1200px) {
    .photo-sessions {
        grid-template-columns: repeat(2, 1fr);
    }
}
</style>
