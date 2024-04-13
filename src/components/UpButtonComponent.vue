<template>
    <div class="up_btn_main_component" @click="handleClick">
        <i class="fa-solid fa-angle-up"></i>
    </div>
</template>
<script setup>

const handleClick = ()=>{
window.scrollTo({top:0,behavior:'smooth'})}

</script>
<style scoped>
.up_btn_main_component{
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