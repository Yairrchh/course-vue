<script setup>
import { ref, onUpdated } from 'vue';

const el = ref('Hello world')

const updateMessage = () => {
  el.value = 'Update message'
}


  onUpdated(() => {
    console.log('onUpdate: the components has been update', el.value )
  })

</script>

<template>
  <div >
      {{ el }}
  </div>
  <button @click="updateMessage">Update Message</button>
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