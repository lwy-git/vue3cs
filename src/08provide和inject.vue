<script setup >
    import centerCom from '@/components/center-com.vue'
import { provide,ref } from 'vue';
// 1.跨层传递普通数据
    provide('the-color','red')
    // 2.跨层传递响应式数据
    const count=ref(100)
    provide('count',count)
    setTimeout(()=>{
        count.value=500
    ,2000})
    // 3.跨层函数传递=>给子代传递可修改的数据
    provide('changeCount',(newcount)=>{
        count.value=newcount
    })
</script>
<template>
    <div>
        <h1>顶层组件</h1>
        <centerCom></centerCom>
    </div>
</template>