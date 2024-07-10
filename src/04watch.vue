<script setup>
    import {ref,watch} from 'vue'
    const count=ref(0)
    const name=ref('qq')
    const changeCount=()=>{
        count.value++
    }
    const changeName=()=>{
        name.value='oo'
    }
    // watch侦听器
    // 1.监视单个数据
    // watch(ref对象，(newValue,oldValue)=>{...})
    // watch(count,(newValue,oldValue)=>{
    //     console.log(newValue,oldValue);
    // })
    // 2.监视多个数据
    // watch([ref1,ref2],(newArra,oldArra)=>{...})
    // watch([count,name],(newArr,oldArr)=>{
    //     console.log(newArr,oldArr);
    // })
    // 3.immediate (一进页面就立即监视)
    //  watch(count,(newValue,oldValue)=>{
    //  console.log(newValue,oldValue);
    //  },{
    //     immediate:true
    //  }
    //  )
    // ————————————————————————————————————
    // 4.deep深度监视，默认的watch是浅层监视
    // 简单类型可以直接监视，复杂类型内部数据变化无法监视
     const userInfo=ref({
        name:'kk',
        age:18
     })
    const changeUserInfo=()=>{
        userInfo.value.age++
    }
    // deep深度监听
    // watch(userInfo,(newValue)=>{
    //     console.log(newValue);
    // },{
    //     deep:true
    // }
    // )
    // 5.对于对象中的单个属性，进行监视
    watch(()=>userInfo.value.age,(newValue,oldValue)=>{
        console.log(newValue,oldValue);
    })
</script>
<template>
    <div>
        {{ count }}
    </div>
    <button @click="changeCount">改数字</button>
    <div>{{ name }}</div>
    <button @click="changeName">改姓名</button>
    <hr>
    <div>{{ userInfo }}</div>
    <button @click="changeUserInfo">修改信息</button>
</template>