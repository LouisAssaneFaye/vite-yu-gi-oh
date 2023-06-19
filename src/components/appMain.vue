<template>
    <main>
        
        <div class="main-up">
            <select name="languages" id="lang">
                <option value="Allen">Allen</option>
                <option value="Other_player">Other_player</option>
            </select>
        </div>

        <div class="main-down">

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
    height: calc(100vh - 70px);
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
}

    
</style>