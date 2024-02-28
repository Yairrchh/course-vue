<script setup>
import { onBeforeMount,  } from 'vue';

    onBeforeMount(() => {
    console.log('onBeforeMount: the components has been onBeforeMount' )
    })
</script>

<template>
    <ul>
        <li>opt1</li>
        <li>opt2</li>
        <li>opt3</li>
    </ul>
</template>