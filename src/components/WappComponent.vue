<template>
    <div class="wapp_main_container">
        <i class="fa-brands fa-whatsapp"></i>

    </div>
</template>
<script setup>



</script>
<style scoped>
.wapp_main_container{
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