<template>
    <div>
        <h1>父传子{{message}}</h1>
        <select>
            <option v-for="p in str" :key="p">{{p}}</option>
        </select>
        <input type="button" @click="send" value="发送子组件的数据" />
        <input type="button" @click="cs" value="改变样式" />
    </div>
</template>

<script setup>
    import {defineProps} from 'vue'
    // 给子组件定义一个message属性，用来接收父组件中的msg
    /*eslint-disable*/
    const props = defineProps({
        message: {
            type: String,
            default: ''
        },
        str: {
            type: Array,
            default: []
        }
    })
    const txt = 'hehe';
    // 实现子传父：
    // 1、在子组件中绑定对应的事件
    // 2、定义emit(自定义事件)
    // 3、在绑定的事件函数中触发emit，并且将子组件中的数据传过去
    // 4、切换到父组件中,绑定自定义事件的处理函数，
    // 事件处理函数的第一个参数就是子组件中发送过来的数据
    const emit = defineEmits(['onSend','onCss'])
    const send = () => {
        emit('onSend',txt);
    }
    
    const css = {
        bg: 'red',
        w: '100px',
        h: '100px'
    }
    // const emit = defineProps(['onCss'])
    const cs = () => {
        emit('onCss',css);
    }


</script>

<style>

</style>