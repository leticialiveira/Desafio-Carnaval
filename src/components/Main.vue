<script setup>
    
</script>

<template>
  <div class="titleCenter">
    <p>Blocos recomendados</p>
    <div class="button-select">
      <button>LISTA</button>
      <button>MAPA</button>
    </div>
  </div>
  
</template>

<style scoped>
.titleCenter {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-bottom: 50px;
}

.titleCenter p {
  color: var(--color-title-main);
  font-weight: 700;
  font-size: 32px;
}

.button-select {
  border: solid 1px var(--border-button-select);
  padding: 8px;
  width: 190px;
  height: 48px;
  display: flex;
  align-items: center;
  border-radius: 6px;
}
.button-select button:nth-last-of-type(2) {
    background-color: var(--bg-button-select-2);
    padding: 4px 24px;
    gap: 8px;
    border-radius: 5px;
    width: 86px;
    height: 32px;
    color: var(--color-button-select-2);
    border: 0;
}

.button-select button:nth-last-of-type(1) {
  padding: 4px 24px;
  gap: 8px;
  border-radius: 5px;
  width: 88px;
  height: 32px;
  background-color: var(--bg-button-select-1);
  color: var(--color-button-select-1);
  border: 0;
}


</style>
