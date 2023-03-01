<script setup>
import HeaderVue from "./components/Header.vue";
import Lists from "./components/Main.vue";
import CardVue from "./components/Card.vue";
import jsonCard from "./mock/cards.json";
import { ref } from "vue";

  
  const name = ref("");
  const city = ref("");
  let filteredCards = ref(jsonCard);

  // Quando a gente faz uma função, precisamos falar o que essa função retorna, então coloquei um return no filteredCards, para dizer que, a função updateFilteredCards() vai retornar o valor dele
  // Porém, filter também é uma função, e ele não conseguiu retorna o que tinha dentro de filter, já que lá não existia um return, então quando o que fizemos foi
  // Retorne o filteredCards dentro de updateFilteredCards() e quero também que me retorne o resultado do meu filter.
  function updateFilteredCards() {
   return filteredCards.value.filter(item => {
    return (
      // Quando você usa || você ta falando que ou vai existir, o title ou o address 
      // Quando você coloca o &&, você diz que, pode existir ambos sozinhos, como 
      // Os dois juntos, ou seja, podemos pesquisar usando os dois
      item.title.toUpperCase().includes(name.value.toUpperCase()) &&
      item.address.toUpperCase().includes(city.value.toUpperCase())
    )
   })
  }

</script>

<template>
  <Header-vue v-model:name="name" v-model:city="city" />
  <div class="main">
    <Lists />
    <div class="grid-cards">
      <CardVue
        v-for="item in updateFilteredCards()"
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
