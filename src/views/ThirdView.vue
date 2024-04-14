<template>
    <div class="thirdview_main_container">
        <h1>Trabajos</h1>
        <img src="foto5.png" alt="" id="foto5" class="wow animate__animated animate__fadeIn">
        <section class="song">
            <i class="fa-solid fa-chevron-left wow animate__animated animate__fadeInLeft" ></i>
            <img :src="selectedSong.cover" alt="" id="cover" :class="{'--playSong':showPlayBtn}" @mouseover="showPlayBtn = true" @mouseleave="showPlayBtn = false" class="wow animate__animated animate__fadeInUp">
            <i class="fa-solid fa-chevron-right wow animate__animated animate__fadeInRight"></i> 
            <i v-if="showPlayBtn" class="fa-regular fa-circle-play"  @mouseover="showPlayBtn = true"></i>
            <p id="band_name" class="wow animate__animated animate__fadeInRight">{{selectedSong.bandName}} - {{ selectedSong.song }}</p>
        </section>
        <section class="all_songs">
            <div v-for="song of data" :key="song.id" class="cover_allsongs" @click="handleSelect(song)">
                <img :src="song.cover" alt="" id="img_cover_all_songs"  :class="{ 'selectedSong': song.id === selectedSong.id}">
            </div>
        </section>
    </div>
</template>
<script setup>
import { ref } from 'vue';
import data from "../assets/data.js"

const selectedSong = ref(data[0])

const showPlayBtn = ref(false)


const handleSelect = (song)=>{
    selectedSong.value = song
    };

</script>
<style scoped>
.thirdview_main_container{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    
}
h1{
    font-family: var(--font1);
    color: white;
    position: absolute;
    top: 50px;
}
#foto5{
    object-fit: cover;
    width: 100%;
    height: 100%;
}
.song{
    width: 100%;
    height: 300px;
    position: absolute;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.fa-chevron-left,.fa-chevron-right{
    color: rgb(124, 124, 124);
    font-size: 40px;
}
.fa-chevron-left:hover,.fa-chevron-right:hover{
    color: white;
    cursor: pointer;
    transition: .2s all ease-in-out;
}
#cover{
    height: 65%;

}
#band_name{
    color: rgb(229, 229, 229);
    position: absolute;
    font-size: 20px;
    font-family: Arial, Helvetica, sans-serif;
    bottom: 10px;
    letter-spacing: 1px;
}
#play{
    width: 70px;
    position: absolute;
}

.--playSong{
    filter: brightness(0.6)!important;
    transition: .3s all ease-in-out;
}
.fa-circle-play{
    color: white;
    font-size: 65px;
    position: absolute;
    cursor: pointer;   
}
.all_songs{
    display: none;
}
@media(min-width:1000px){
#cover{
    height: 80%;
}
#band_name{
    bottom: 0px;
}
.song{
    height: 340px;
}
.all_songs{
    display: unset;
    width: 70%;
    height: 130px;
    position: absolute;
    bottom: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
}
.cover_allsongs{
    width: 104px;
    height: 80%;
    border-radius: 3px;
    background-color: green;
    user-select: none;
}
#img_cover_all_songs{
    width: 100%;
    height: 100%;
    filter: brightness(0.4)
}
#img_cover_all_songs:hover{
    cursor: pointer;
    transition: .4s all ease-in-out;
    filter: brightness(1)!important;
}
.selectedSong {
    filter: brightness(1)!important;
    transition: .4s all ease-in-out;
}
}

</style>