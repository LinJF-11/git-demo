<template>
    <div>
        <h1>黄金戒指</h1>
        <slot :lv="f"></slot>
    </div>
</template>

<script setup>
    import {ref} from 'vue';
    const f = ref('祖母绿');
</script>

<style>
    
</style>