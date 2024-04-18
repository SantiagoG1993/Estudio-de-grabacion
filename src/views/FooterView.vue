<template>
    <div class="footer_main_container">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5269.362023035176!2d-59.67161837774124!3d-33.69626350247232!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95ba2325f19105af%3A0xaa0bd2b4ec93e84c!2sChivilcoy%202745%2C%20San%20Pedro%2C%20Provincia%20de%20Buenos%20Aires!5e0!3m2!1ses!2sar!4v1713039450739!5m2!1ses!2sar" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        <Logo  id="logo"/>
        <section class="info1">
            <h3>ESTUDIO DE GRABACION G-SOUND</h3>
            <ul>
                <li @click="handleClick(0)">Home</li>
                <li @click="handleClick(0.5)">Servicios</li>
                <li @click="handleClick(2)">Trabajos</li>
                <li @click="handleClick(3)">Contacto</li>
                <li @click="handleClick(3)">Envianos un mensaje</li>
            </ul>
        </section>
        <section class="info2">
            <p><i class="fa-solid fa-envelope"></i> estudiogsound@gmail.com</p>
            <p><i class="fa-solid fa-phone"></i> +54 9 341 2475871</p>
            <p><i class="fa-brands fa-instagram"></i> /gsoundestudio</p>
            <p><i class="fa-brands fa-square-facebook"></i> /estudiogsound</p>
        </section>


    </div>
</template>
<script setup>
import Logo from '../components/Logo.vue'


const handleClick = (number)=>{
    const vh = window.innerHeight
    window.scrollTo(
        {
            top:`${vh*number}`,
            behavior:'smooth'
        }
    )
}
</script>
<style scoped>
.footer_main_container{
    width: 100%;
    height: 100vh;
    background-color: #1A1A1A;
    display: flex;
    flex-direction: column;
    align-items: start;
    
}
iframe{
    width: 100%;
    height: 40vh;
}
h3{
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    margin-left: 5%;
}
ul{
    display: flex;
    flex-direction: column;
    gap: 8px;
    list-style-type: none;
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    margin-left: 5%;
    margin-top: 30px;
}
ul li:hover{
    cursor: pointer;
    color: rgb(190, 190, 190);
    transition: .2s all ease-in-out;
}
.info2{
    display: flex;
    flex-direction: column;
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    margin-left: 5%;
    margin-top: 30px;
    gap: 8px;
}

@media (min-width:1000px){
.footer_main_container{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    position: relative;
}
#logo{
    position: absolute;
    bottom: 46%;
}
.info1{
    margin-left: 5%;
    width: 300px;
}
h3{
    width: 370px;
}
.info2{
    margin-top: 4%;
}
}
</style>