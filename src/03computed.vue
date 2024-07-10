<script setup>
import {computed,ref} from 'vue'
const list=ref([1,2,3,4,5,6])
const computedList=computed(()=>{
    return list.value.filter(item=>item>2)
})
// 
// 定义一个修改数组的方法
const addList=()=>{
    list.value.push(666)
}
// const count = ref(1)
// const plusOne = computed(() => count.value + 1)

// console.log(plusOne.value) 
// const count = ref(1)
// const plusOne = computed({
//   get: () => count.value + 1,
//   set: (val) => {
//     count.value = val - 1
//   }
// })

// plusOne.value = 1
// console.log(count.value)
</script>
<template>
    <div>
        <div>原数组：{{ list }}</div>
        <div>过滤数组：{{ computedList }} </div>
        <button @click="addList">修改数组</button>
    </div>
</template>