<template>
    <main>
        
        <div class="main-up">
            <selectMain />
        </div>

        <div class="main-down">
            <div class="first-container">
                <div class="second-container">
                    <div class="second-container-up">
                        <span>
                            Found 39 cards
                        </span>
                    </div>
                    <div class="second-container-down">
                        <cards :cardList="cardList" />
                    </div>

                </div>

            </div>

        </div>

    </main>
</template>
<script>
import cards from './cards.vue';
import selectMain from './selectMain.vue';
import axios from 'axios';
export default { 
    name: 'appMain',
    data(){
        return{
            cardList:[],
        }
        
    },
    components: {
        cards,
        selectMain,
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
main{
    background-color: $orangeColor;
    div.main-up{
        height: 70px;
        border: 1px solid black;
        display: flex;
        align-items: center;
        
    }

    div.main-down{
        div.first-container{
            width: 86%;
            margin: 0 auto;
            background-color: $whiteColor;
            padding-top: 55px;
            div.second-container{
                width: 94%;
                margin: 0 auto;
                div.second-container-up{
                    display: flex;
                    align-items: center;
                    height: 55px;
                    background-color: $blackColor;
                    color: $whiteColor;
                    font-size: 1.2rem;
                    padding-left: 1rem;
                }
                div.second-container-down{
                    @include flex();
                    
                }
                
            }
        }
    }
}

    
</style>