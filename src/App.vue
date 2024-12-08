<template>

  <!--Step 3 use the component-->
  <!-- <img alt="Music playlist" src="https://tse4.mm.bing.net/th?id=OIP.xLz7v1QbFN-ocBnJfu2g3wHaFP&pid=Api&P=0&h=180" width="100%" height="300"> -->
  <div class="header-container">
    <!-- Display the image -->
    <img
      alt="Music playlist"
      src="https://tse4.mm.bing.net/th?id=OIP.xLz7v1QbFN-ocBnJfu2g3wHaFP&pid=Api&P=0&h=180"
      class="header-image"
    />
    <!-- Display the header text -->
    <h1 class="header-text">Music Playlist</h1>
    <img
      alt="Music playlist"
      src="https://tse4.mm.bing.net/th?id=OIP.xLz7v1QbFN-ocBnJfu2g3wHaFP&pid=Api&P=0&h=180"
      class="header-image"
    />
  </div>
  <div class="container">
    <MyHeader title="Dynamite" singer="BTS" albumName="BE" songDuration="3:19" image="https://images.genius.com/df009633e4702b3838c793c7fd97adf3.1000x1000x1.png" releasedDate="August 21,2020"/> 
    <Playlist :songs=songs />
  </div>
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import Playlist from './components/Playlist.vue';


export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    Playlist
  },
  data(){
    return {
      songs: []
    }
  },
  methods:{
    //promoises
    async fetchPlaylist(){
      const res = await fetch('https://hemalatha-ganipisetti-node.onrender.com/api ');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.songs = await this.fetchPlaylist();
  }

}
</script>


<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');


body {
  font-family: 'Montserrat', sans-serif;
  text-align: center;
}
.header-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  margin-bottom: 20px;
  border: 2px solid snow;
}

.header-image {
  width: 42%;
  height: 100px;
  object-fit: cover;
  /* border-radius: 50%; */
}

.header-text {
  font-size: 24px;
  font-weight: bold;
  color: #051e26;
}
.container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 16px;
        padding: 20px;
        background-color: ghostwhite;
    }
div{
  margin-bottom: 0.5em;

}


</style>
