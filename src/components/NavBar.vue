<template>
    <header>
        <div class="logo">
            <img src="../assets/skorup-logo.png" alt="skorupski-photo" />
        </div>

        <nav>
            <ul class="nav-links">
                <li class="nav-item">
                    <a href="#" class="nav-link">About Me</a>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">Blog</a>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">Gallery</a>
                </li>
            </ul>
        </nav>
        <Button class="cta">
            <template #cta>Contact</template>
        </Button>
    </header>
</template>
<script setup>
import Button from "../reusable/Button.vue";
</script>
<style scoped>
header {
    display: flex;
    align-items: center;
    justify-content: flex-end;

    padding: 1rem 0;

    /* background-color: hsl(0, 0%, 95%); */
    color: var(--color-font);
}

.logo {
    height: 50px;
    cursor: pointer;
    margin-right: auto;
}

.nav-links {
    display: flex;
    gap: 3rem;
}

.nav-item:hover {
    color: var(--color-accent);
}

.cta {
    margin-left: 3rem;
    background-color: var(--color-accent);
    color: white;
}
</style>
