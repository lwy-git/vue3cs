<!-- <script >
// setup比beforeCreate执行更早，获取不到this
// 数据和函数，需要在setup里最后return才能在模块里用
export default{

  setup(){
    console.log('setup');
   const a='hello vue3'
   const loga=()=>{
    console.log(a);
   }
   return {
    a,
    loga
   }
  },
  beforeCreate(){
console.log('beforeCreate');
  }
}
</script> -->
<script setup>
 const a='hello vue3'
   const loga=()=>{
    console.log(a);
   }
</script>
<template>
  <div>
    {{ a }}
  </div>
  <button @click="loga"></button>
</template>