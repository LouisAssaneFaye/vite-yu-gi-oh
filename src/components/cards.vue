<template>
    
    <singleCard v-for="cardObj in cardList"
    :cardElement= "cardObj"
    />
    

</template>

<script>
import singleCard from './singleCard.vue';
export default {
    name: 'cards',
    data(){
        return{

        }
    },
    components:{
        singleCard
    },
    props:{
        cardList: Array
    },
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    
</style>