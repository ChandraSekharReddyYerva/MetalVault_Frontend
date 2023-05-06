<template>
  <MyHeader metalName="Metal Vault" authorName="Chandra Sekhar Reddy Yerva" />

  <MetalBox :metals="metals" />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MetalBox from  './components/MetalBox.vue'

export default {
  name: 'App',
  components: {
    // Step 2 register the component 
    MyHeader,
    MetalBox
  },

  data(){
    return {
      metals: []
    }
  },
  methods: {
    // promises

      async fetchMetals(){
         const res= await fetch('https://chandrayerva.onrender.com/api')
         const data= await res.json()
          //console.log(data)
         return data
      }

  },

  async created(){
    this.metals = await this.fetchMetals()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: #293241;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>
