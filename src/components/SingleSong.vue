<template>
    <div>

      <img :src="song.image" alt="cover" width="100%" height="400px" />
      <h2> {{song.title}} </h2>
      <h4> Singer: <span>{{song.singer }}</span></h4>
      <h4> Album: <span>{{song.albumName}}</span> </h4>
      <h4> Song Duration: <span>{{ song.songDuration }}</span></h4>
      <h4> Released Date: <span>{{song.releasedDate}}</span></h4>
    </div>
</template>

<script>

export default{
    name: 'SingleBook',
    props:{
        song: Array
    }
}
</script>

<style>
        span{
            font-weight: 590;
        }
</style>