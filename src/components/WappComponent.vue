<template>
    <div v-if="scrollPosition >90" class="wapp_main_container">
        <i class="fa-brands fa-whatsapp"></i>

    </div>
</template>
<script setup>
import {ref} from 'vue';

const scrollPosition = ref(0)

window.addEventListener('scroll',()=>{
    scrollPosition.value = window.scrollY
})


</script>
<style scoped>
.wapp_main_container{
    animation: fadeInRight .6s;
    width: 65px;
    height: 65px;
    border-radius: 50%;
    background-color: rgb(83, 169, 83);
    position: fixed;
    bottom: 30px;
    right: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
    box-shadow: 12px 13px 22px -14px rgba(0,0,0,0.75);
}
.wapp_main_container:hover{
    background-color: rgb(59, 121, 59); 
    cursor: pointer;
    transition: .3s all ease-in-out;
}
i{
    font-size: 40px;
    color: white;
}

</style>