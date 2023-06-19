<template>
    <main>
        <cards />
    </main>
</template>
<script>
import cards from './cards.vue';
export default {
    name: 'appMain',
    data(){
        
    },
    components: {
        cards
    }
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

    
</style>