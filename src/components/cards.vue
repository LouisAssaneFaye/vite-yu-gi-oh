<template>
    
    <singleCard v-for="cardObj in cardList"
    :cardElement= "cardObj"
    />
    

</template>

<script>
import singleCard from './singleCard.vue';
import axios from 'axios';
export default {
    name: 'cards',
    data(){
        return{
            cardList: [
               
                
                
            ]

        }
    },
    components:{
        singleCard
    },
    created(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then( (response) => {
        console.log(response);
        this.cardList = response.data.data;
        })
        .catch(function (error) {
        // handle error
        console.log(error);
        })

    },
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    
</style>