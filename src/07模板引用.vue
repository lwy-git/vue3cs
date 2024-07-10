<script setup>
import TestCom from '@/components/test-com.vue'
import { onMounted,ref } from 'vue';
// 模块引用（可以获取dom,也可以获取组件）
// 1.调用ref,生成ref对象
// 2.通过ref标识,进行绑定
// 3.通过ref对象.value即可访问到要绑定的元素
const inp=ref(null)
onMounted(()=>{
    // 一进页面渲染完就聚焦
    // console.log(inp.value);
    // inp.value.focus()
})
const clickFn=()=>{
    inp.value.focus()
}
// -----------------------------
const com=ref(null)
const getCom=()=>{
    // 访问测试组件
    // console.log(com.value);
    // 访问组件中的属性或者方法
    console.log(com.value.count);
    com.value.sayHi()
}
</script>
<template>
    <div>
        <input ref="inp" type="text" name="" id="">
   <button @click="clickFn">点击输入框聚焦</button>
   </div>
   <TestCom ref="com"></TestCom>
   <button @click="getCom">获取组件</button>
</template>