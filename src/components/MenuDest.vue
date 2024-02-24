<script setup>
import { onUnmounted } from 'vue';

    onUnmounted(() => {
    console.log('onUnmounted: the components has been onUnmounted' )
    })
</script>

<template>
    <ul>
        <li>opt1</li>
        <li>opt2</li>
        <li>opt3</li>
    </ul>
</template>