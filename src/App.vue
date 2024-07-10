<script setup>
    import MyInput from '@/components/my-input.vue'
import { ref } from 'vue';

    const txt=ref('12345')
</script>
<template>
    <div>
        <MyInput v-model="txt"></MyInput>
        {{ txt }}
    </div>
</template>