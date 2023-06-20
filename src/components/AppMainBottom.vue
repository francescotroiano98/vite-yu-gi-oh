<template>
<section class="main-bottom-container">

    <div class="container main-bottom">
        <h2 class="m-0 px-1 py-2">Found {{ cardsFounded }} cards</h2> <!--QUI NON E' CORRETTO USARE LO STORE-->
        <YuGiOhDeck/>
    </div>

</section>
    
</template>
<script>

import YuGiOhDeck from '../components/YuGiOhDeck.vue';
export default {
    data(){
        return{
            
        }
    },
    props : {
        cardsFounded : Number,

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