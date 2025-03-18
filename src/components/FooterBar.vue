<script setup lang="ts">
import IconGithub from './icons/IconGithub.vue';
</script>

<template>
    <div class="footer">
        <a href="https://github.com/RoyHcnnz/PasswordGenerator">Source Code <IconGithub /></a>
    </div>
</template>

<style scoped>
    .footer{
        height: 50px;
        border-top: solid 1px var(--color-primary-trans);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .footer p{
        font-family: "Courier Prime", monospace;
    }
    a {
        color: inherit; /* blue colors for links too */
        text-decoration: inherit; /* no underline */
    }
    a:hover{
        color: var(--color-primary-light-20)
    }

</style>