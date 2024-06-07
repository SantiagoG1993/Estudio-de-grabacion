<template>
    <div class="contact_main_container wow animate__animated animate__fadeIn">
        <h1>Contacto</h1>
        <section>
            <p><strong>Telefono:</strong> +54 9 341 2475871</p>
            <p><strong>Email:</strong> gsoundestudio@gmail.com</p>
            <p><strong>Direccion:</strong> Chivilcoy 2745 - San Pedro, Buenos Aires, Argentina</p>
        </section>
    
        <ContactForm /> 


    </div>
</template>
<script setup>
import ContactForm from '../components/ContactForm.vue'


</script>
<style scoped>
.contact_main_container{
    width: 100%;
    height: 100vh;
    background-color: #C8D2BF;
    display: flex;
    flex-direction: column;
    align-items: center;
}
h1{
    font-family: Arial, Helvetica, sans-serif;
    font-size: 50px;
    font-weight: 100;
    align-self: flex-start;
    margin-left: 10%;
}
p{
    font-family: Arial, Helvetica, sans-serif
}
section{
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 30px;
    margin-top: 10px;
    margin-bottom: 40px;
}
@media(min-width:1000px){
    .contact_main_container{
    flex-direction: row;
    justify-content: center;
    gap: 60px;
    position: relative;
}
section{
    width: auto;
    margin-top: 0px;
    margin-bottom: 0px;
    align-self: start;
    margin-top: 9.5%;
    gap: 55px;
}
p{
    display: flex;
    flex-direction: column;
    justify-content: center;
}h1{
    position: absolute;
    left: 0px;
    top: 7%;

}
}
</style>