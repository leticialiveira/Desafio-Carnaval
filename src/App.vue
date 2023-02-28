<script setup>
import HeaderVue from "./components/Header.vue";
import Lists from "./components/Main.vue";
import CardVue from "./components/Card.vue";
import jsonCard from "./mock/cards.json"

</script>

<template>
  <Header-vue />
  <div class="main">
    <Lists />
    <div class="grid-cards">
      <CardVue v-for="item in jsonCard" :key="item.title" :title="item.title" :description="item.description"
        :address="item.address" :image="item.image" />
    </div>
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

.grid-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  width: 100%;
  height: auto;
}
</style>
