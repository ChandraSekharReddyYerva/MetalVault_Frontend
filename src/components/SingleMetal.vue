<template>
    
    <div  :class="metal.Availability ? 'yes': 'no' ">

                    <h2>Metal Name: {{ metal.Metal }}</h2>
                    <h4>Short Name: {{ metal.ShortName }}</h4>
                    <h4>Price in USD: {{ metal.Price }}</h4>
                    <a :href="metal.URL" target="_blank">Click here for Metal Details</a>
                    <h4>Date: {{ metal.Date }}</h4>

    
    



    </div>
</template>

<script>

export default{
    name: 'SingleMetal',
    props:{
        metal: Array
    }
}
</script>

<style scoped>



.yes{
    background-color: #98C1D9;
}

h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    grid-gap: 1em;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}

.no{
background-color: #E0FBFC !important;

}

a {
    text-decoration: none;
    color: blue;
}

a:hover {
    background-color: white;
    text-decoration: underline;
}


</style>
