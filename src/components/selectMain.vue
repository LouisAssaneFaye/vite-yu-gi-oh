<template>
   <select name="languages" id="lang">
                <option value="Allen">Allen</option>
                <option value="Other_player">Other_player</option>
    </select>
</template>
<script>
export default {
    name: 'selectMain',
    data() {
        return{
           

        }
    },
    
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