<template>
    <div class="index_main_container">
        <NavBarComponent/>
        <div class="img_container">
            <img src="foto1.png" alt="" id="foto1" class="animate__animated animate__fadeIn">
            <p id="estudio" class="animate__animated animate__slideInDown">ESTUDIO JOG</p>
            <p id="subtitle" class="animate__animated animate__slideInUp">Estudio de grabacion y produccion musical</p>
        </div>
        <div class="services animate__animated animate__fadeInUp">
            <ul >
                <li>GRABACION MULTIPISTA</li>
                <li>MEZCLA</li>
                <li>MASTERING</li>
                <li>PRODUCCION MUSICAL</li>
            </ul>
        </div>

    </div>
</template>
<script setup>
import NavBarComponent from '../components/NavBarComponent.vue'


</script>
<style scoped>
.index_main_container{
    width: 100%;
    height: 100vh;
    background-color: #5B783E; 
    display: flex;
    flex-direction: column;
    align-items: center;
}
#foto1{
    width: 100%;
    height: 100%;
    object-fit: cover;
    
}
.img_container{
    width: 100%;
    height: 65vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

}
#estudio{
    font-family: var(--font1);
    font-size: 40px;
    color: white;
    position: absolute;
    top: 35vh;
}
#subtitle{
    position: absolute;
    color: white;
    font-family: "KoHo", sans-serif;
    font-size: 22px;
    width: 80%;
    top: 40vh;
    text-align: center;
}
.services{
    margin-top: 43px;
}
.services ul{
    list-style-type: none;
    color: white;
    font-family: var(--font1);
    display: flex;
    flex-direction: column;
    gap: 20px;
    font-size: 24px;
}
</style>