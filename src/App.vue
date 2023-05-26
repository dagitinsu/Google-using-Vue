<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Body from './components/Body.vue'
import Footer from './components/Footer.vue'

import { ref } from 'vue';

const imageVisible = ref(true);

const toggleImageVisibility = () => {
  imageVisible.value = !imageVisible.value;
};
;
</script>

<template>
  <Header @buttonClicked="toggleImageVisibility"/>
  <Body :isVisible="imageVisible"/>
  <Footer />
  

 
</template>

<style scoped>

</style>
<components>
  <ButtonComponent />
  <ImageComponent :isVisible="imageVisible" />
</components>
