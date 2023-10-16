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
  max-width: 1060px;
  height:auto;
  margin: 0 auto;
  padding: 30px 20px;
  background-color: rgb(200, 218, 224);
}
</style>