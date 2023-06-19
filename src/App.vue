<script>
import appHeader from './components/appHeader.vue';
import appMain from './components/appMain.vue';
export default {
  name:'app',
  components:{
    appHeader,
    appMain,
  }
}
</script>
  
<template>
  <appHeader />
  <appMain />
</template>

<style lang="scss">
     @import './styles/general.scss';
</style>