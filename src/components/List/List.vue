<script setup>

const images = [
  { name: 'Whitewater', image: '/src/assets/images/whitewater.jpg' },
  { name: 'Nightpanther', image: '/src/assets/images/nightpanther.jpg' },
  { name: 'Krakengard', image: '/src/assets/images/krakengard.jpg' },
  { name: 'Wolfthorn', image: '/src/assets/images/wolfthorn.jpg' },
]

const emit = defineEmits(['image-selected']);
emit('image-selected', images[0]);

</script>

<template>    
    <div class="c-list">
        <h1 v-for="image in images" @mouseover="$emit('image-selected', image)">{{ image.name }}</h1>
    </div>
</template>

