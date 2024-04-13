<template>
    <div class="projects_main_container">
        <section class="images">
            <img src="foto2.png" alt="">
            <img src="foto3.png" alt="">
            <img src="foto4.png" alt="" id="foto4">
        </section>

    </div>
</template>
<script setup>



</script>
<style scoped>
.projects_main_container{
    width: 100%;
    height: 100vh;
    background-color: #314121; 
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

}
.images{
    width: 90%;
    display: flex;
    flex-direction: column;
    gap: 20px;
    height: 90%;
    align-items: center;
}
.images img{
    width: 80%;
    height: 33%;
    object-fit: cover;
}
</style>