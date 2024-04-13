<template>
    <div class="thirdview_main_container">
        <h1>Trabajos</h1>
        <img src="foto5.png" alt="" id="foto5">
        <section class="song">
            <i class="fa-solid fa-chevron-left"></i>
            <img src="cover1.jpg" alt="" id="cover" :class="{'--playSong':showPlayBtn}" @mouseover="showPlayBtn = true" @mouseleave="showPlayBtn = false">
            <i class="fa-solid fa-chevron-right"></i> 
            <img v-if="showPlayBtn" src="play.png" alt="" id="play" >
            <p id="band_name">Espectros- Abismos</p>
        </section>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const showPlayBtn = ref(false)


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
.song i{
    color: rgb(124, 124, 124);
    font-size: 40px;
}
.song i:hover{
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
</style>