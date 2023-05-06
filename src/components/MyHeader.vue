<template>
  <div>
      <h1> {{metalName}} </h1>
      <h4> {{authorName}} </h4>
      
  </div>
  </template>
  
  <script>
  
  export default{ // Exporting Default Object
      name: 'MyHeader',
      props:{ 
          authorName:String,
          metalName:String
      }
  }
  
  </script>
  
  <style scoped>
  
  div{
      text-align: center;
      color: aliceblue;
      background-color: #3D5A80;
      padding: 5px;
  }
  
  </style>