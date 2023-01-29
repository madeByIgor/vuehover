<script setup>
    import img1 from '../../assets/images/whitewater.jpg';
    import img2 from '../../assets/images/nightpanther.jpg';
    import img3 from '../../assets/images/krakengard.jpg';
    import img4 from '../../assets/images/wolfthorn.jpg';

    const props = defineProps(['index'])
    const images = [img1, img2, img3, img4]
</script>

<template>
    <div class="c-images">
        <div class="c-images__wrapper">
            <template v-for="(img, i) in images">
                <img :src="img" v-if=" i === props.index ? true : false" />
            </template>   
        </div>
    </div>    
</template>

