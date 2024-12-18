<script setup>
    const signedIn = false;
</script>

<template>
    <header>
        <a href="index.html">
            <h1>MG Archived</h1>
        </a>
        <nav>
            <a href="">Games</a>
            <a v-if="!signedIn" href="">Sign In</a>
            <a v-else-if="signedIn" href="">Profile</a>
        </nav>
    </header>
</template>

<style scoped>
    header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 70px;
        width: 100%;
        background-color: var(--header-bg);
    }

    header > a {
        margin-left: 20px;
    }

    header a {
        color: var(--header-fg);
        text-decoration: none;
    }

    header a:hover {
        text-decoration: underline;
    }

    nav {
        margin-right: 20px;
    }
</style>
