<script setup>
import { ref } from 'vue';
import List from './components/List/List.vue';
import Images from './components/Images/Images.vue';

const imageToShow = ref({});

</script>

<template>

  <div class="wrapper">
    <List @image-selected="(img) => imageToShow = img" />
    <Images :image-to-show="imageToShow"/>
  </div>
 
</template>
