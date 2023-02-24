<script setup>
import HeaderVue from "./components/Header.vue";
import Lists from "./components/Main.vue";
</script>

<template>
  <Header-vue />
  <div class="main">
    <Lists />
  </div>
</template>

<style scoped>
.main {
  gap: 40px;
  width: 70vw;
  margin: 0 auto;
  margin-top: 100px;
  height: auto;
  background-color: var(--bg-content-input);
  /* border: solid 1px red; */
}
</style>
