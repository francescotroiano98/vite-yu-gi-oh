<template>
    <section class="main-top-container">
        <div class="container main-top d-flex         align-items-center px-4">
                <select class="form-select" aria-label="Default     select example">
                    <option selected>Scegli il tuo archetipo</option>
                    <option v-for="archetipo in cardsArchetypeList" :value="archetipo[0].archetype_name">{{ archetipo[0].archetype_name }}</option>
                    <option value="2">Noble Knight</option>
                    <option value="3">Melodius</option>
                </select>
        </div>
    </section>    
</template>
<script>
import axios from 'axios';
export default {
    data(){
        return{
            
            cardsArchetypeList:[],
            archetypes:[]
            
        }
        
    },
    name:"AppMainTop",
    methods: {

        serchedArchetypeList(){
            
            axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
            .then((response) => {

                   this.cardsArchetypeList.push(response.data)

                   


                 
                 
            })
            
        }


        

    },
    created(){
        this.serchedArchetypeList()
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