<script setup >
    const props=defineProps({
        car:String,
        money:Number
    })
    const emit=defineEmits(['changeMoney'])
    const buy=()=>{
    //  通过emit触发
    emit('changeMoney',5)
    }
</script>
<template>
    <div class="son">
        我是子组件-{{ car }}-{{ money }}
        <button @click="buy">花钱</button>
    </div>
</template>
<style  scoped>
      .son{
        border: 5px solid green;
        padding: 30px;
      }
</style>