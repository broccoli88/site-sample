<template>
    <NavBarMobile v-if="isNavMobile" />
    <NavBar v-else />
    <main>
        <RouterView />
    </main>
    <Footer></Footer>
</template>

<script setup>
import { RouterLink, RouterView } from "vue-router";
import NavBarMobile from "./components/NavBarMobile.vue";
import NavBar from "./components/NavBar.vue";
import Footer from "./components/Footer.vue";
import { onMounted, onUpdated, ref } from "vue";

// check for displaying mobile or desktop navbar

const isNavMobile = ref(null);
const check = () => {
    if (window.innerWidth >= 800) {
        isNavMobile.value = false;
    } else {
        isNavMobile.value = true;
    }
};

const checkInitialWindowWidth = onMounted(check);
window.addEventListener("resize", check);
</script>

<style scoped>
main {
    min-height: 100vh;

    padding: 16rem 0;
}
</style>
