<template>
<section class="main-bottom-container">

    <div class="container main-bottom">
        <h2 class="m-0 px-1 py-2">Found {{ store.cardsList.length }} cards</h2>
        <YuGiOhDeck/>
    </div>

</section>
    
</template>
<script>
import {store} from '../store'
import YuGiOhDeck from '../components/YuGiOhDeck.vue';
export default {
    data(){
        return{
            store
        }
    },
    name: "AppMainBottom",
    components: { 
        YuGiOhDeck }
}
</script>
<style lang="scss" scoped>
    .main-bottom-container{

        background-color: orange;

        .main-bottom{
            background-color: white;
            padding: 2rem;
            display: flex;
            flex-direction: column;

            h2{
                background-color: black;
                color: white;
                font-size: 1.5rem;
            }


        }

    }

</style>