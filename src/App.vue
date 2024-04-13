<template>
    <div class="app_container">
        <IndexView />
        <ImagesView />
        <ThirdView />
        <ContactView />
        <UpButtonComponent />
        <WappComponent />
    </div>

</template>

<script setup>
import IndexView from './views/IndexView.vue'
import ImagesView from './views/ImagesView.vue'
import ThirdView from './views/ThirdView.vue'
import ContactView from './views/ContactView.vue'
import UpButtonComponent from './components/UpButtonComponent.vue'
import WappComponent from './components/WappComponent.vue'
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
