<template>
   
    <div v-for="metal of metals.MetalDetails" :key="metal.id">

       
        <SingleMetal :metal="metal" />

    </div>
    
    
</template>
<script>
import SingleMetal from "./SingleMetal.vue"

export default {
    name: 'MetalBox',
    props:{
        metals: Array
    },
    components: {
        SingleMetal
    }
    
}
</script>

<style scoped>
.metalbox{

    background-color: bisque;
    padding: 1em;
    color: gray;
    margin: auto;
}
</style>