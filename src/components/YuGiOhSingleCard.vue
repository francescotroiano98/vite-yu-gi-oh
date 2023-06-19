<template>
        <div class="_mycardsize text-center card mb-3">
            <img :src="imageLink" class="card-img-top" alt="...">
  
                <div class="card-body d-flex flex-column justify-content-between">
                    <h5 class="card-title">{{ name }}</h5>
                        <p class="card-text">{{ type }}</p>
                    
                </div>
        </div>

</template>
<script>
export default {
    name:"YuGiOhSingleCard",
    data(){
        return{

        }
    },
    props : {
        imageLink : String,
        name: String,
        type: String

    }
    
}
</script>
<style lang="scss" scoped>
    ._mycardsize{
        width: calc(100% / 5.5);
        .card-body{
            background-color: orange;

            h5{
                color: white;
                font-weight: bold;
                font-size: 1rem;
            }
            p{
                font-size: 0.9rem;
            }
        }

        
        
    }
</style>