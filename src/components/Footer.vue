<template>
    <footer>
        <section class="contact">
            <span>&copy; Skorupski Photo 2022</span>
            <span>jon.doe@gmail.com</span>
            <span>+48 666 666 666</span>
        </section>
        <section class="media">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-instagram"></i>
        </section>
    </footer>
</template>

<style scoped>
footer {
    padding: 1.5rem 0;

    display: flex;
    justify-content: space-between;
}

.contact {
    display: none;
}

.media {
    flex: 1;
    display: flex;
    justify-content: flex-start;
    gap: 1.5rem;
}

.media i {
    width: 1.6rem;

    color: var(--color-font);

    cursor: pointer;

    transition: 0.4s all ease;
}

.media i:hover {
    color: var(--color-accent);
}

@media (min-width: 900px) {
    .contact {
        display: flex;
        align-items: center;

        flex: 4;
    }
    .contact span {
        font-size: clamp(1rem, 1.2vw, 1.2rem);
        font-weight: 400;
        color: var(--color-font);
        letter-spacing: 1.2px;
        text-transform: uppercase;

        position: relative;
    }

    .contact span:nth-child(1) {
        padding-right: 3rem;
        margin-right: 1.5rem;
    }

    .contact span:nth-child(2),
    .contact span:nth-child(3) {
        padding: 0 3rem;
    }

    .contact span:nth-child(2)::before,
    .contact span:nth-child(3)::before {
        content: "";
        display: block;

        position: absolute;
        width: 16px;
        height: 2px;
        top: 50%;
        left: 0;

        transform: translateY(-50%);

        background-color: var(--color-accent);
    }

    .contact span:first-child::after {
        content: "";
        display: block;

        position: absolute;
        width: 2px;
        height: 100%;
        top: 0;
        right: 0;

        background-color: var(--color-font-light);
    }

    .media {
        justify-content: flex-end;
    }
}
</style>
