<template>
    <div class="navbar_main_container animate__animated animate__fadeIn"  :class="{ '--showNavModal': menuIsVisible,'--transparent':scrollPosition>150 && currentWidth >999 }"  ref="containerRef" v-if="scrollPosition<2600">
        <Logo id="logo" class="animate__animated animate__fadeInLeft" @click="handleClick(0)"/>
        <ul class="desktop_menu animate__animated animate__fadeInRight" v-if="scrollPosition<2600">
            <li @click="handleClick(0)"   :class="{'--dark':scrollPosition > vh*3}">Home</li>
            <li @click="handleClick(0.5)" :class="{'--dark':scrollPosition > vh*3}">Servicios</li>
            <li @click="handleClick(2)"   :class="{'--dark':scrollPosition > vh*3}">Trabajos</li>
            <li @click="handleClick(3)"   :class="{'--dark':scrollPosition > vh*3}">Contacto</li>
        </ul>
        <i class="fa-solid fa-bars" @click="menuIsVisible = !menuIsVisible"></i>
        <ul v-if="menuIsVisible" class="modal_menu">
            <li @click="handleClick(0)">Home</li>
            <li @click="handleClick(0.6)">Servicios</li>
            <li @click="handleClick(2)">Trabajos</li>
            <li @click="handleClick(3)">Contacto</li>
        </ul>
    </div>
</template>
<script setup>
import Logo from '../components/Logo.vue'
import {ref} from 'vue';
import { onClickOutside } from '@vueuse/core'
const containerRef = ref(null)
const menuIsVisible = ref(false)


const scrollPosition = ref(0)
const currentWidth = ref(0)

window.addEventListener('scroll',()=>{
    currentWidth.value = window.innerWidth

})

window.addEventListener('scroll',()=>{
    scrollPosition.value = window.scrollY

})

onClickOutside(containerRef,()=>{
    menuIsVisible.value = false
})

const vh = window.innerHeight

const handleClick = (number)=>{
    menuIsVisible.value = false
    window.scrollTo(
        {
            top:`${vh*number}`,
            behavior:'smooth'
        }
    )
}
</script>
<style scoped>
.navbar_main_container{
    width: 100%;
    height: 105px;
    background-color: #1D270C;
    position: fixed;
    top: 0px;
    z-index: 1000;
}
.desktop_menu{
    display: none;
}
#logo{
    margin-bottom: 15px;
}
.--transparent{
    background-color: transparent;
    transition: .8s all ease-in-out;
}
.--showNavModal{
    transition: .3s all ease-in;
    height: 335px!important;
}
.--dark{
    color: #1D270C;
    transition: .2s all ease-in-out;
}
i{
    position: absolute;
    top: 35px;
    right: 25px;
    color: white;
    font-size: 35px;
}
i:active{
    color: #4e622b;
}
.modal_menu{
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-left: 45px;
    margin-top: 30px;
    list-style-type: none;
}
ul li{
    color: white;
    font-family: var(--font1);
    font-size: 20px;
}

@media(min-width:1000px){
    .fa-bars{
        display: none;
    }
    .navbar_main_container{
    display: flex;
    justify-content: end;
    align-items: center;
    height: 90px;
}
    .desktop_menu{
        display: unset;
        display: flex;
        justify-content: center;
        align-items: center;
        list-style-type: none;
        gap: 30px;
        margin-right: 10%;
    }
    .desktop_menu li:hover{
        color: rgb(185, 185, 185);
        transition: .3s all ease-in-out;
        cursor: pointer;
    }

#logo{
    position: absolute;
    left: 3%;
}
#logo:hover{
    cursor: pointer;
    filter: brightness(1.3);
}


}

</style>