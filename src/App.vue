<script setup>
import { ref } from 'vue';
import List from './components/List/List.vue';
import Images from './components/Images/Images.vue';

const index = ref('')

  function passIndex(i) {
    index.value = i;
  }

</script>

<template>

  <div class="wrapper">
    <List :handler="passIndex" />
    <Images :index="index"/>
  </div>
 
</template>
