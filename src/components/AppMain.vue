<template>
    <div>
        <h2>{{ store.cardsList.data }}</h2>
        <AppMainTop/>
        <AppMainBottom/>
    </div>
</template>
<script>
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
        
    },
    created (){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {

            store.cardsList = response.data

            console.log(response.data)

            
        })
    }
}


</script>
<style lang="scss">
    
</style>