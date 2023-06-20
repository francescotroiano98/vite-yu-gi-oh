<template>
    <div class="d-flex flex-wrap justify-content-between" >
        
            <YuGiOhSingleCard v-for="singleCard in store.cardsList"
                :imageLink="singleCard.card_images[0].image_url"
                :name="singleCard.name"
                :type="singleCard.archetype"/>
                    
    </div>
</template>
<script>
import YuGiOhSingleCard from './YuGiOhSingleCard.vue';
import {store} from '../store'
export default {

    data(){
        return{
            store
        }
    },
    
    name: "YuGiOhDeck",
    components:{
        YuGiOhSingleCard
    }
}
</script>
<style lang="scss" scoped>


h3{color: red;}
    
</style>