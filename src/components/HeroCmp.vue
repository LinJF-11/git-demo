<template>
    <div>
        <slot name="weap" :ur="user" :win="winRate"></slot>
        <h2>{{user.name}}</h2>
        <slot name="shield" :win="winRate"></slot>
    </div>
</template>

<script setup>
    import {reactive,ref} from 'vue';
    // 将user对象传递到插槽中，在template标签中使用user的值
    const user = reactive({
        name: '嬴政',
        emp: '中路'
    });
    const winRate = ref('65%');
</script>

<style>

</style>