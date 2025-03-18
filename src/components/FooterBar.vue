<script setup lang="ts">
import IconGithub from './icons/IconGithub.vue';
</script>

<template>
    <div class="footer">
        <p>Source Code <IconGithub /></p>
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
</style>