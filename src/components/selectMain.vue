<template>
   <select v-model="selected" name="languages" id="lang">
                <option v-for="cardObj in cardList" value="" @click="$emit('searched',selected)">
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
            selected: '',
            

        }
    },
    methods:{
        
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