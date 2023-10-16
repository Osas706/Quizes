<script setup>
import {RouterView} from "vue-router";
</script>

<template>
  <div class="container">
    <RouterView />
  </div>
</template>

<style scoped>
.container{
  max-width: 1020px;
  height:100vh;
  margin: 20px auto;
}
</style>