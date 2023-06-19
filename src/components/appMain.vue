<template>
    <main>
        
        <div class="main-up">
            <select name="languages" id="lang">
                <option value="Allen">Alien</option>
                <option value="Other">Other</option>
            </select>
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
                        <cards />
                    </div>

                </div>

            </div>

        </div>

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
main{
    background-color: $orangeColor;
    div.main-up{
        height: 70px;
        border: 1px solid black;
        display: flex;
        align-items: center;
        select{
            height: 2rem;
            width: 9rem;
            margin-left: 6rem;

        }
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