<template>
    <!-- 为了能够让子组件内部能够拿到父组件中定义的数据， -->
    <!-- 我们就可以通过给子组件定义一个属性来接收这个数据 -->
    <div>
        <child-cmp :message="msg" :str="str" @onCss="tocs" @onSend="deal"/>
        <div class="my">牛耳软件学院</div>
        <color-cmp @onCl="col"/>
        <div :style="cl" >Hello world</div>
    </div>
</template>

<script setup>
    import ChildCmp from './ChildCmp.vue';
    import ColorCmp from './ColorCmp.vue';
    import {ref,reactive} from 'vue';
    const msg = ref('Hello world');
    const str = ref(['语文','数学','英语']);
    const deal = (val) => {
        console.log(val);
    }

    const so = reactive({});
    const tocs = (val) => {
        console.log(val)
        so.backgroundColor = val.bg;
        so.width = val.w;
        so.height = val.h;
    }

    const cl = reactive({});
    const col = val => {
        cl.color = val
        // console.log(val);
    }
</script>

<style >
    .my{
        background-color: v-bind('so.backgroundColor');
        width: v-bind('so.width');
        height: v-bind('so.height');
    }
</style>