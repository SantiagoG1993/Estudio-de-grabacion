<template>
    <div class="loader_main_container">
        `   <video src="bg-logo_1.mp4" autoplay muted loop></video>`
    </div>
</template>
<script setup>

</script>
<style scoped>
.loader_main_container{
    user-select: none;
    width:100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 0px;
    z-index: 5000;
    background-color: white;
    animation: change-opacity 3s ease-in;
}
video{
    width: 180px;
    height: 180px;
}
@keyframes change-opacity{
    0% {
        opacity: 1;
    }
    90%{
        opacity: 1;
    }
    100%{
        opacity: 0;
    }
}
</style>