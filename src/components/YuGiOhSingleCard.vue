<template>
    <div>
        <div class="card mb-3">
            <img :src="imageLink" class="card-img-top" alt="...">
  
                <div class="card-body">
                    <h5 class="card-title">{{ name }}</h5>
                        <p class="card-text">{{ type }}</p>
                    
                </div>
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
<style lang="">
    
</style>