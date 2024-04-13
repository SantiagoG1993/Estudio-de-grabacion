<template>
    <div class="navbar_main_container"  :class="{ '--showNavModal': menuIsVisible }" ref="containerRef">
        <Logo />
        <i class="fa-solid fa-bars" @click="menuIsVisible = true"></i>
        <ul v-if="menuIsVisible">
            <li>Home</li>
            <li>Servicios</li>
            <li>Trabajos</li>
            <li>Contacto</li>
        </ul>
    </div>
</template>
<script setup>
import Logo from '../components/Logo.vue'
import {ref} from 'vue';
import { onClickOutside } from '@vueuse/core'
const containerRef = ref(null)
const menuIsVisible = ref(false)

onClickOutside(containerRef,()=>{
    menuIsVisible.value = false
})
</script>
<style scoped>
.navbar_main_container{
    width: 100%;
    height: 105px;
    background-color: #1D270C;
    position: fixed;
    top: 0px;
    z-index: 1000
}
.--showNavModal{
    transition: .3s all ease-in;
    height: 335px!important;
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
ul{
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


</style>