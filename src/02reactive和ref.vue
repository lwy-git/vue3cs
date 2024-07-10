<script setup>
// ref:接收简单类型或复杂类型返回一个响应式对象
// 本质：在原有传入数据的基础上，外层包了一层对象，包层了复杂结构
// 底层：包成复杂对象后借助reactive实现的响应式
// 脚本js中访问数据，需要通过.value
// 在template中不需要.value
import {ref} from 'vue'
const count=ref(0)
const addCount=()=>{
 count.value++
}
</script>
<template>
    <div>

       <div>{{ count }}</div> 
       <button @click="addCount">+1</button>
    </div>
</template>