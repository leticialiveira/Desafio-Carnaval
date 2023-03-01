<script setup>
import HeaderVue from "./components/Header.vue";
import Lists from "./components/Main.vue";
import CardVue from "./components/Card.vue";
import jsonCard from "./mock/cards.json";
import { ref } from "vue";
import axios from "axios";



// O axios se utiliza usando alguns parametros:
// - method: GET, POST, PUT, DELETE
// - url: url da requisição
// - data: dados a serem enviados
// - config: configurações da requisição
// - headers: configurações de headers
// - params: configurações de parametros

// - GET -> requisição GET - Você pega o JSON
// - POST -> requisição POST - Você envia o JSON
// - PUT -> requisição PUT - Você atualiza o JSON
// - DELETE -> requisição DELETE - Você deleta o JSON

// Aqui estamos pegando o JSON do servidor e transformando em um array de objetos
// axios.get -> pega o JSON do servidor e transforma em um array de objetos

// Estamos acessando o json que esta dentro dessa URL
// Se a requisição não der erro, ele vai entrar dentro do .then

axios.get("https://api.tvmaze.com/shows")
.then((response) => {
  // Aqui a gente pega o resultado do JSON, que é o próprio JSON
  // Se você abrir o site e da console, você vai ver o que está dentro do JSON
  console.log(response.data);
});
  // 240 array
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
