<script setup>
const props = defineProps(['handler'])
const btnList = ['Whitewater', 'Nightpanther', 'Krakengard', 'Wolfthorn']

const handlerOut = function(e) {
    console.log('im out')
}
</script>

<template>    
    <div class="c-list">
        <h1 v-for="(item, i) in btnList" :key="item" @mouseover="props.handler(i)" @mouseout="handlerOut">{{ item }}</h1>
    </div>
</template>

