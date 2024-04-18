<template>
    <div class="contact_form_main_container wow animate__animated animate__fadeInRight">
        <h3>ENVIANOS UN MENSAJE</h3>
        <form action="https://formsubmit.co/gamarras1993@gmail.com" method="POST">
            <label for="">Nombre
                <input type="text" class="input_text" name="name">
            </label>
            <label for="">Email
                <input type="text" class="input_text" name="email">
            </label>
            <label for="">Mensaje
                <input type="text" class="input_text_msg" name="message">
            </label>
            <button type="submit">Enviar</button>
            <input type="hidden" name="_captcha" value="false">
        </form>
    </div>

</template>
<script setup>



</script>
<style scoped>
.contact_form_main_container{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;   
}
h3{
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 200;
    align-self: flex-start;
    margin-left: 5%;
    margin-bottom: 10px;
}
form{
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-top: 10px;
}
label{
    display: flex;
    flex-direction: column;
    justify-content: center;
    font-family: Arial, Helvetica, sans-serif;
    gap: 5px; 
    margin-bottom: 15px;
}
.input_text{
    height: 45px;
    background-color: #D9D9D9;
    border: none;
}
.input_text_msg{
    height: 120px;
    background-color: #D9D9D9;
    border: none;
}
.input_text:focus,.input_text_msg:focus{
    outline: none;
    padding-left: 20px;
    background-color: #e8e8e8;  
}
button{
    width: 100px;
    height: 35px;
    background-color: #5B783E;
    color: white;
    border: none;
    border-radius: 3px;
    align-self: flex-end;
    margin-top: 10px
}
button:hover{
    background-color: #899e72;    
    cursor: pointer;
    transition: .1s all ease-in-out;
}
@media(min-width:1000px){
    .contact_form_main_container{
        width: 700px;
    }
    form{
    width: 100%;
    display: flex;
    margin-top: 0px;
}
    .input_text,.input_text_msg{
        background-color: #d1d5cc;
    }
    .input_text:focus,.input_text_msg:focus{
        background-color: #8c997e;
        transition: .3s all ease-in-out;
    }
    .input_text:hover,.input_text_msg:hover{
        cursor: pointer;
      outline: 1px solid #7f8d71;
    }
    h3{
        margin-left: 0px;
    }
}

</style>