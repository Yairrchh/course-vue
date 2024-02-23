<script setup>
import { ref, onMounted } from 'vue';


const greeting = 'Hello vue.js'
const el = ref('Hello world')


  onMounted(() => {
    console.log('onMounted: el componente ah sido montado', el.value )
  })

</script>

<template>
  <div ref="el">
      {{ greeting }}
  </div>
</template>

<style scoped>
.fade-leave-to {
  opacity: 0;
}

.fade-leave-active,
.fade-from-active {
  transition: opacity 0.5s ease;;
}
</style>