<template>
  <div class="songCard">
      <img :src="image" alt="cover" width="100%" height="400px" />
      <h2> {{title}} </h2>
      <h4> Singer: <span> {{ singer }}</span></h4>
      <h4> Album: <span>{{albumName}} </span></h4>
      <h4> Song Duration: <span>{{ songDuration }} </span></h4>
      <h4> Released Date: <span>{{releasedDate}} </span></h4>
  </div>
  </template>
  
  <script>
  
  export default{ // Exporting Default Object
      name: 'MyHeader',
      props:{ 
  
          title:String,
          singer:String,
          albumName: String,
          songDuration:String,
          image:String,
          releasedDate:String
      }
  }
  
  </script>
  
  <style scoped>
  
  div{
      text-align: center;
  }
  
  </style>
