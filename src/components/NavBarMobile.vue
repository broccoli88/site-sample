<template>
    <header>
        <div class="nav-top">
            <div class="logo">
                <img src="../assets/skorup-logo.png" alt="skorupski-photo" />
            </div>
            <div class="menu-mobile" @click="toggleMobileNav">
                <i class="fa-solid fa-bars"></i>
            </div>
        </div>

        <nav :class="{ navActive: navMobileActive }" class="navbar">
            <ul class="nav-links-mobile">
                <li class="nav-item-mobile">
                    <a href="#" class="nav-link-mobile">About Me</a>
                </li>
                <li class="nav-item-mobile">
                    <a href="#" class="nav-link-mobile">Blog</a>
                </li>
                <li class="nav-item-mobile">
                    <a href="#" class="nav-link-mobile">Gallery</a>
                </li>
                <li class="nav-item-mobile">
                    <a href="#" class="nav-link-mobile">Contact</a>
                </li>
            </ul>
            <div class="nav-media-mobile">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-instagram"></i>
            </div>
        </nav>
    </header>
</template>
<script setup>
import { ref } from "vue";

const navMobileActive = ref(null);
const toggleMobileNav = () => {
    navMobileActive.value = !navMobileActive.value;
    const header = document.querySelector("header");
    if (navMobileActive.value === true) {
        header.style.height = "42rem";
    }
    if (navMobileActive.value === false) {
        header.style.height = "7rem";
    }
};
</script>
<style scoped>
header {
    display: flex;
    flex-direction: column;
    padding: 1rem 10%;

    background-color: white;

    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 7rem;
    z-index: 9;

    overflow: hidden;

    transition: 0.5s all ease;
}

.nav-top {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    height: 50px;
    cursor: pointer;
}

.menu-mobile .fa-solid {
    font-size: 3rem;
    color: var(--color-accent);
    cursor: pointer;
}

.navbar {
    background-color: var(--color-main);

    display: flex;
    flex-direction: column;

    padding: 3rem 0;
}

.nav-item-mobile {
    padding: 0.5em 0;
    color: var(--color-font);
}

.nav-litem-mobile a,
.nav-media-mobile i {
    transition: 0.4s all ease;
}

.nav-item-mobile a:hover,
.nav-media-mobile i:hover {
    color: var(--color-accent);
}

.nav-media-mobile {
    width: 100%;
    margin-top: 8rem;

    display: flex;
    justify-content: center;
    gap: 1.5rem;
}

.nav-media-mobile i {
    color: var(--color-font);
    cursor: pointer;
}
</style>
