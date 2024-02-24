<script setup>
import { ref } from 'vue';
import MenuDest from './components/MenuDest.vue'

let onUnmountedComponents = ref(true);

const onUnmountedMessage = () => {
  console.log('unUnmounted component')
  onUnmountedComponents.value = !onUnmountedComponents.value;

}

</script>

<template>
  <button @click="onUnmountedMessage">unUnmounted</button>
  <div >
    <MenuDest v-if="onUnmountedComponents"/>
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