<script setup>
import { ref } from 'vue';
import List from './components/List/List.vue';
import Images from './components/Images/Images.vue';

const images = [
  { name: 'Whitewater', image: '/src/assets/images/whitewater.jpg' },
  { name: 'Nightpanther', image: '/src/assets/images/nightpanther.jpg' },
  { name: 'Krakengard', image: '/src/assets/images/krakengard.jpg' },
  { name: 'Wolfthorn', image: '/src/assets/images/wolfthorn.jpg' },
]

const imageToShow = ref({});

</script>

<template>

  <div class="wrapper">
    <List :images="images" @image-selected="(img) => imageToShow = img" />
    <Images :image-to-show="imageToShow"/>
  </div>
 
</template>
