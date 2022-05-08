<template>
    <div>
        <!-- <nav>
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
       ,
                        ParentCmp,
                        HeroCmp,
                        RingCmp </nav>
        <router-view/> -->
        <!-- 只要是有插槽的组件，都必须写成双标签的形式 -->
        <!-- 原因就是组件双标签之间的内容会替换掉<slot></slot>标签 -->
        <!-- <ring-cmp>
            <template #default="slotProps">
                <button>{{slotProps.lv}}</button>
            </template>
        </ring-cmp> -->
        <!-- <hero-cmp > -->
            <!-- slotProps 是一个对象，包含了slot插槽的所有属性 -->
            <!-- {ur: {name: '嬴政',emp: '中路'}} -->
            <!-- <template v-slot:weap="slotProps">
                <h1>倚天剑{{slotProps.ur.emp}}{{slotProps.win}}</h1>
            </template>
            <template #shield="slotProps">
                <h1>天龙盾{{slotProps.win}}</h1>
            </template>
        </hero-cmp> -->
        <parent-cmp />
    </div>
    
</template>

<script setup>
    // import HeroCmp from './components/HeroCmp.vue';
    // import RingCmp from './components/RingCmp.vue';
    import ParentCmp from './components/ParentCmp.vue';

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


</style>
