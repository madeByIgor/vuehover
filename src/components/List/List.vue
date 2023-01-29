<script setup>
const props = defineProps(['images'])
const emit = defineEmits(['image-selected']);
emit('image-selected', props.images[0]);

</script>

<template>    
    <div class="c-list">
        <h1 v-for="image in images" @mouseover="$emit('image-selected', image)">{{ image.name }}</h1>
    </div>
</template>

