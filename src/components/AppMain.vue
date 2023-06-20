<template>
    <main>
        <div v-if="cardList = store.cardsList.length">
            <AppMainTop/>
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
            store
        }
    },
    name:"AppMain",
    components:{
        AppMainTop,
        AppMainBottom,
        RotateCircle

        
    },
    methods: {
        serchedList(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {

            store.cardsList = response.data.data

            

           

            
        })

        }


        

    },
    created (){
        this.serchedList()
    }
}


</script>
<style lang="scss">
    
</style>