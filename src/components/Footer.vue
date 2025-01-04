<script setup>
    const signedIn = false;
    const link = "";
</script>

<template>
    <footer>
        <div>
            <h1>
                My Games Archived is a place where different
                people can enjoy the games I've created by myself or
                with with other amazing people (all linked in the credits)
            </h1>
            <h6>@ 2024 My Games Archived</h6>
        </div>
        <nav>
            <div>
                <h2>Navigation :</h2>
                <ul>
                    <li>
                        <router-link to="/">
                        Games
                        </router-link>
                    </li>
                    <li v-if="!signedIn"><a v-bind:href="link" target="_blank">
                        Sign In
                    </a></li>
                    <li v-else-if="signedIn"><a href="">
                        Profile
                    </a></li>
                    <li v-else-if="signedIn"><a href="">
                        Dashboard
                    </a></li>
                </ul>
            </div>
            <div>
                <h2>Resources :</h2>
                <ul>
                    <li><a target="_blank" href="https://github.com/4lex16">
                        GitHub
                    </a></li>
                    <li><a target="_blank" href="">
                        Repository
                    </a></li>
                </ul>
            </div>
        </nav>

    </footer>
</template>

<style scoped>
    footer {
        display: flex;
        justify-content: space-between;
        align-content: center;
        color: var(--footer-fg);
        background-color: var(--footer-bg);
        padding: 20px 0 20px 20px;
    }

    footer > div {
        display: flex;
        flex-direction: column;

        width: 600px;
    }

    footer > div > h1 {
        font-size: 20pt;
        margin: 0 0 20px 0;
    }


    footer > nav {
        display: flex;
        justify-content: space-around;

        width: 400px;
    }


    footer > nav a {
        color: var(--footer-fg);
        text-decoration: none;
    }

    footer > nav a:hover {
        text-decoration: underline;
    }

</style>