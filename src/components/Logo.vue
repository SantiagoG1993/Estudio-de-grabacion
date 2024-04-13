<template>
    <div class="logo_main_container">
        <div class="logo_circle">
            <img src="faders.svg" id="faders" alt="">
        </div>
        <p id="jog">JOG</p>
        <p id="subtitle">Estudio de grabacion</p>

    </div>
</template>
<script setup>
    


</script>
<style scoped>
.logo_main_container{
    height: 105px;
    width: 160px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;

}
.logo_circle{
background-color: #2B4108;
    width: 46px;
    height: 46px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
}
#faders{
    width: 25px;
}
#jog{
    font-family: var(--font1);
    font-weight: 400;
    color: white;
    font-size: 24px;
    font-style: normal;
}
#subtitle{
    font-family: var(--font1);
    color: white;
    font-size: 12px;
    position: absolute;
bottom: 14px;
    letter-spacing: 1px;
}

</style>