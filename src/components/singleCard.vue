<template>
   
   <div class="card">
        <div class="img">
           <img :src="cardElement.card_images[0].image_url" alt="immagine">
        </div>
    
        <div class="text">
    
            <span class="title">
                {{cardElement.name}}
            </span>
 
            <span class="type">
                {{cardElement.archetype}}
            </span>

        </div>

   </div>
  
</template>

<script>
export default {
    name: 'singleCard',
    props:{
        cardElement: Object,
    }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

div.card{
    width: 17.3%;
    height: 24rem;
    border: 1px solid black;
    margin-bottom: 1.3rem;
    div.img{
        height: 75%;
        border: 1px solid black;
        img{
            width: 100%;
        }
    }
    div.text{
        background-color: $orangeColor;
        height: 25%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        
        span.title{
            color: $whiteColor;
            font-size: 1rem;
            margin-top: -3px;
            margin-bottom: 18px; 
            margin-left: 1.2rem
            
        }
        span.type{
            margin: 0 auto;
        }
    }
}
    
</style>