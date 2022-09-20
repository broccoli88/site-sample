<template>
    <button>
        <a href="#">
            <slot name="cta"></slot>
        </a>
    </button>
</template>
<script setup></script>
<style scoped>
button {
    background-color: transparent;
    border: 0;
    padding: 0.3em 2em;

    font-size: 1.6rem;
    font-family: var(--font-poppins);
    font-weight: 500;

    cursor: pointer;
}

button:hover {
    filter: opacity(0.95);
}
</style>
