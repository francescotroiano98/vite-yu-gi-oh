<template>
    <main>
        <div v-if="cardList = store.cardsList.length">
            <AppMainTop @myarchetype="getCardsFromFilter"/>
            <AppMainBottom :cardsFounded="store.cardsList.length"/>
        </div>
        <div v-else>
            <RotateCircle/>
        </div>
        
    </main>    
</template>
<script>
import RotateCircle from './RotateCircle.vue'
import AppMainTop from './AppMainTop.vue';
import AppMainBottom from './AppMainBottom.vue';
import {store} from '../store'
import axios from 'axios';
export default {
    data(){
        return{
            store,
            apiUrl : 'https://db.ygoprodeck.com/api/v7/cardinfo.php',
        }
    },
    name:"AppMain",
    components:{
        AppMainTop,
        AppMainBottom,
        RotateCircle

        
    },
    methods: {
        getCardsFromFilter(filter){
            axios.get(this.apiUrl, {
                params: {
                    num: 20,
                    offset: 0,
                    archetype : filter
                }
            })

                    .then((response) => {

                                            this.store.cardsList = response.data.data
                    })

                }


        

    },
    created (){
        this.getCardsFromFilter()
    }
}


</script>
<style lang="scss">
    
</style>