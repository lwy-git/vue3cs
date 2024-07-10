<script setup>
    import { onMounted } from 'vue'
    const getList=()=>{
        setTimeout(()=>{
           console.log('发送请求，获取数据');
        },1000)
    // console.log(1);
    }
    getList()
    onMounted(()=>{
        console.log('onMounted生命周期钩子函数-逻辑1');
    })
    // 写成函数的调用方式，可以调用多次
    onMounted(()=>{
        console.log('onMounted生命周期钩子函数-逻辑2');
    })
</script>
<template>
    <div>
        
    </div>
</template>