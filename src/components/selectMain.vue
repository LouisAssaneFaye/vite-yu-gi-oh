<template>
   <select name="languages" id="lang">
                <option v-for="cardObj in cardList" value="" @click="logContent()">
                    {{ cardObj.archetype }}
                </option>
                
    </select>
</template>
<script>
export default {
    name: 'selectMain',
    props:{
        cardList: Array,
    },
    data() {
        return{
           

        }
    },
    methods:{
        logContent(){
            console.log('ciao');
        }
    }
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

select{
    height: 2rem;
    width: 9rem;
    margin-left: 6rem;

}
    
</style>