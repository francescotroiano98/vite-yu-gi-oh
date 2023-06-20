<template>
    <section class="main-top-container">
        <div class="container main-top d-flex         align-items-center px-4">
                <select class="form-select" aria-label="Default     select example">
                    <option selected>Scegli il tuo archetipo</option>
                    <option v-for="archetipo in archetypes">{{ archetipo.archetype_name }}</option>
                </select>
        </div>
    </section>    
</template>
<script>
import axios from 'axios';
export default {
    data(){
        return{
            
            
            archetypes:[]
            
        }
        
    },
    name:"AppMainTop",
    methods: {

        searchedArchetypeList(){
            
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {

                this.archetypes = response.data;

                   


                 
                 
            })
            
        }


        

    },
    created(){
        this.searchedArchetypeList()
        console.log(this.cardsArchetypeList)
    }
    
}


</script>
<style lang="scss" scoped>
.main-top-container{

    background-color:orange;
    height: 100px;
        .main-top{
            height: 100%;
            
            
                h2{
                    color:white

                }
        }
}    
</style>