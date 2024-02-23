<script setup>
import MenuDest from "./components/MenuDest.vue"
import { ref } from "vue";
import ModalDest from "./components/ModalDest.vue";

const show = ref(false)

</script>

<template>
  <button @click="show = !show">Menu</button>
  <Transition name="fade">
    <MenuDest v-show="show"/>
  </Transition>
  <div>
    <ModalDest/>
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