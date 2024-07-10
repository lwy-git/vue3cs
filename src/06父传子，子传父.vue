<script setup>
    // 父传子
    // 1.给子组件添加属性的方式传值
    // 2.在子组件中，通过props接受

    // 子传父
    // 1.在子组件内部，emit触发事件(编译器鸿定义)
    // 2.在父组件，通过@监听
    import {ref} from 'vue'
    import sonCom from '@/components/son-com.vue'
    const money=ref(100)
    const addMoney=()=>{
        money.value+=10
    }
    const changeFn=(newValue)=>{
        money.value=newValue
    }
</script>
<template>
    <div>
        <h3>父组件-{{ money }}
        <button @click="addMoney">赚钱</button>
        </h3>
        <sonCom 
        @changeMoney="changeFn"
        car="奥迪" 
        :money="money"></sonCom>
    </div>
</template>