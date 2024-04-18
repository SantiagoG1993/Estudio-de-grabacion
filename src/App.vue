<template>
    <div class="app_container">
        <Loader v-if="isVisibleLoader == true" />
        <IndexView v-if="isVisibleIndex == true" />
        <ImagesView v-if="isVisibleIndex == true" />
        <ThirdView v-if="isVisibleIndex == true" />
        <ContactView v-if="isVisibleIndex == true" />
        <UpButtonComponent />
        <WappComponent />
        <FooterView v-if="isVisibleIndex == true" /> 
    </div>

</template>

<script setup>
import IndexView from './views/IndexView.vue'
import ImagesView from './views/ImagesView.vue'
import ThirdView from './views/ThirdView.vue'
import ContactView from './views/ContactView.vue'
import UpButtonComponent from './components/UpButtonComponent.vue'
import WappComponent from './components/WappComponent.vue'
import FooterView from './views/FooterView.vue'
import Loader from './views/Loader.vue'
import 'animate.css'
import { onMounted,ref } from 'vue';
import WOW from 'wow.js'


window.onload = function() {
    // Hace un scroll hacia arriba con una animación suave
    window.scrollTo({
        top: 0,
        behavior: 'instant'
    });
};

const isVisibleLoader = ref(true)
const isVisibleIndex =ref(false)

  document.body.style.overflow='hidden'
onMounted(()=>{
  document.body.style.overflow='hidden'
  setTimeout(()=>{
    isVisibleLoader.value = false
    isVisibleIndex.value = true
    document.body.style.overflow='auto'
    
  },3000)
    const wow = new WOW();
    wow.init()
})
</script>

<style>
:root{
  --font1:"Kelly Slab", sans-serif;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


</style>
