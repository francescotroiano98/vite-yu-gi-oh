<template>
    <div>
        <h2>IL TUO DECK</h2>
        <AppMainTop/>
        <AppMainBottom/>
    </div>
</template>
<script>
import AppMainTop from './AppMainTop.vue';
import AppMainBottom from './AppMainBottom.vue';
export default {
    name:"AppMain",
    components:{
        AppMainTop,
        AppMainBottom
    }
}
</script>
<style lang="scss">
    
</style>