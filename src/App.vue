<script setup>
import { ref, provide } from "vue";
import HomeApp from "./components/HomeApp.vue"

const name = ref('otr')

provide("userName", "yairNeeeerd")

</script>

<template>
  <div>
    <HomeApp :var1="name" var2="Martinez"></HomeApp>
  </div>
</template>
