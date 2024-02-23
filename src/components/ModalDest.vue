<script setup>
import { ref } from 'vue';


const show = ref(false)

const toggle = () => {
    show.value = !show.value;
}

</script>

<template>
    <div>
        <button @click="toggle">
            Modal
        </button>
        <Teleport to="body">

        </Teleport>
    </div>
</template>