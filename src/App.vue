<template>
  <div>
      <AppHeader/>
      <AppMain/>
  </div>
</template>
<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
    name: "App",
    components:{
      AppHeader,
      AppMain
    }
  
}
</script>
<style lang="scss">

@import './styles/general.scss';
@import '../node_modules/bootstrap/scss/bootstrap';
  
</style>