<script setup >
    const count=999
    const sayHi=()=>{
        console.log('hello');
    }
    // 子组件数据暴露出来，父组件才能调用
    defineExpose({
        count,
        sayHi
    })
</script>
<template>
    <div>
        测试组件-{{ count }}
    </div>
</template>