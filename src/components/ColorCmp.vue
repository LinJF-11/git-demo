<template>
    <select @change="tocl">
        <option value="black">请选择皮肤</option>
        <option value="red">红</option>
        <option value="yellow">黄</option>
        <option value="blue">蓝</option>
    </select>
</template>

<script setup>
    import {defineEmits} from 'vue';
    const emit = defineEmits(['onCl']);
    const tocl = (e) => {
        emit('onCl',e.target.value);
    }
</script>

<style>

</style>