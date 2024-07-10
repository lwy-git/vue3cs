<script setup >
import { inject, provide } from 'vue';

    const thecolor=inject('the-color')
    const count1=inject('count')
    const changeCount=inject('changeCount')
    const clickFn=()=>{
        changeCount(1000)
    }
</script>
<template>
    <div>
        <h3>底层组件-{{ thecolor }}-{{ count1 }}</h3>
        <button @click="clickFn">更新count</button>
    </div>
</template>