<template>
    <header>
        <span>
            YU-Gi-Oh Api
        </span>

    </header>
</template>
<script>
export default {
    name: 'appHeader',
    data(){

    }
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
header{
    height: 70px;
    span{
        display: flex;
        height: 100%;
        font-size: 2rem;
        align-items: center;
        margin-left: 5rem;

    }
}
    
</style>