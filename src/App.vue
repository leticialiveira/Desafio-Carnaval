<script setup>
import HeaderVue from "./components/Header.vue";
import Lists from "./components/Main.vue";
import CardVue from "./components/Card.vue";
import jsonCard from "./mock/cards.json";
import { ref } from "vue";

const name = ref("");
const city = ref("");
let filteredCards = ref(jsonCard);

let resultCards = filteredCards.value.filter(
  (item) =>
    item.title.toUpperCase().includes(name.value.toUpperCase()) ||
    item.address.includes(city.value)
);
console.table(resultCards);
</script>

<template>
  <Header-vue :name="name" :city="city" />
  <div class="main">
    <Lists />
    <div class="grid-cards">
      <CardVue
        v-for="item in resultCards"
        :key="item.title"
        :title="item.title"
        :description="item.description"
        :address="item.address"
        :image="item.image"
        :link="item.link"
      />
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
}
.grid-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  width: 100%;
  height: auto;
}
</style>
