<template>   
        <div v-for="song in songs.slice(1)" :key="song.songId" class="songCard" >
            <SingleSong :song=song />
        </div>

</template>
<script>
import SingleSong from './SingleSong.vue';

export default {
    name: 'MusicPlaylist',
    props:{
        songs: Array
    },
    components:{
        SingleSong
    }
    
}
</script>
<style>
    .songCard {
        width:25%;
        padding:16px;
        border: 2px solid #cde1e7;

    }
</style>
