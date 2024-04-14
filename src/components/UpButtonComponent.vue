<template>
    <div v-if="scrollPosition >90" class="up_btn_main_component" @click="handleClick">
        <i class="fa-solid fa-angle-up"></i>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const handleClick = ()=>{
window.scrollTo({top:0,behavior:'smooth'})}

const scrollPosition = ref(0)

window.addEventListener('scroll',()=>{
    scrollPosition.value = window.scrollY
})
</script>
<style scoped>
.up_btn_main_component{
    animation: fadeInLeft 0.6s;
    width: 60px;
    height: 60px;
    border-radius: 3px;
    background-color: #405025;
    position: fixed;
    bottom: 30px;
    left: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
    box-shadow: 12px 13px 22px -14px rgba(0,0,0,0.75);
    
}
i{
    color: white;
    font-size: 22px;
}
.up_btn_main_component:hover{
    background-color: #9cae7c;
    cursor: pointer;
    transition: .3s all ease-in-out;  
}
</style>