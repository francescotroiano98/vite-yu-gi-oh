<template>
    <div>
        <h3>sono il deck</h3>
            <YuGiOhSingleCard/>
    </div>
</template>
<script>
import YuGiOhSingleCard from './YuGiOhSingleCard.vue';
export default {
    name: "YuGiOhDeck",
    components:{
        YuGiOhSingleCard
    }
}
</script>
<style lang="scss" scoped>

h3{color: red;}
    
</style>