<template>
    <div class="logo">
        <h1>PWD::GEN</h1>
    </div>
</template>

<style scoped>
    .logo{
        width: 100%;
        height: 60px;

        display: flex;
        align-items: center;

        padding-left: 15%;
        font-weight: 800;   
        font-family: "Courier Prime", monospace;

        border-bottom: solid 1px var(--color-primary-trans);
    }
    
    @media only screen and (max-width: 620px) {
        .logo{
            padding-left: 0;
            justify-content: center;
        }
    }
</style>