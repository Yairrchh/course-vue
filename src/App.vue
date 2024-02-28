<script setup>
import { ref } from 'vue';
import MenuDest from './components/MenuDest.vue'

let onUnmountedComponents = ref(false);

const onUnmountedMessage = () => {
  onUnmountedComponents.value = !onUnmountedComponents.value;
  console.log('Click onBeforeMount')
}

</script>

<template>
  <button @click="onUnmountedMessage">OnBeforeMount</button>
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