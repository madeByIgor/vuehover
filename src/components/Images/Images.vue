<script setup>
    const props = defineProps(['imageToShow'])
    console.log(props.imageToShow)
</script>

<template>
    <div class="c-images">
        <div class="c-images__wrapper">
            <img :src="props.imageToShow.image" v-if="!!props.imageToShow" />
        </div>
    </div>    
</template>

