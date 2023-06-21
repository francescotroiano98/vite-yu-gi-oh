<template>
    <section class="main-top-container">
        <div class="container main-top d-flex         align-items-center px-4">
                <select class="form-select" aria-label="Default select example" v-model="selectedFilter"  @change="$emit('myarchetype')">
                    <option selected>Scegli il tuo archetipo</option>
                    <option v-for="cardArchetype in archetypes" :value="cardArchetype.archetype_name">{{ cardArchetype.archetype_name }}</option>
                </select>
        </div>
    </section>    
</template>
<script>
import axios from 'axios';

export default {
    data(){
        return{
            
            selectedFilter:'',
            archetypes:[]
            
        }
        
    },
    name:"AppMainTop",
    methods: {
        

        getArchetypeList(){
            
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {

                this.archetypes = response.data;

            })
            
        }


        

    },
    created(){
        this.getArchetypeList()
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