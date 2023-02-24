<script setup>
</script>
<template>
  <header>
    <div class="content">
      <p>FIND YOUR BLOCK</p>
      <h1>Encontre os <span> melhores blocos </span> de carnaval de 2023</h1>
    </div>
    <div class="content-input">
      <div class="content-input-name">
        <input
          type="text"
          name="name"
          id="name"
          placeholder="Pesquise por nome"
        />
        <img src="../assets/icons/Vector.png" alt="" />
      </div>
      <div class="content-input-city">
        <select id="cidade" name="cidade">
          <option value="">Selecione uma cidade</option>
          <option value="Salvador-BA">Salvador-BA</option>
          <option value="São Paulo-SP">São Paulo-SP</option>
          <option value="Florianópolis-SC">Florianópolis-SC</option>
          <option value="Curitiba-PR">Curitiba-PR</option>
          <option value="Rio de Janeiro-RJ">Rio de Janeiro-RJ</option>
          <option value="Porto Alegre-RS">Porto Alegre-RS</option>
        </select>
        <img src="../assets/icons/Vector (2).png" alt="" />
      </div>
      <button id="button">BUSCAR AGORA</button>
    </div>
    <div class="image-1">
      <img src="../assets/img/g8.png" alt="" />
    </div>
    <div class="image-2">
      <img src="../assets/img/g12.png" alt="" />
    </div>
  </header>
</template>

<style scoped>
header {
  width: 100vw;
  height: 500px;
  background-color: var(--bg-header);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 30px;
  position: relative;
}

header .content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}

header .content p {
  color: var(--color-header-p);
  font-weight: 500;
  font-size: 16px;
}

header .content h1 {
  color: var(--color-header-h1);
  font-weight: 700;
  font-size: 48px;
  width: 647px;
  text-align: center;
}

header .content h1 span {
  color: var(--color-header-h1-span);
}

header .content-input {
  background-color: var(--bg-content-input);
  border: 1px solid var(--border-content-input);
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 40px;
  gap: 24px;
  width: 993px;
  height: 128px;
}

header .content-input input {
  width: 348px;
  height: 48px;
  padding: 12px 8px 12px 40px;
  gap: 12px;
  border-radius: 5px;
  background-color: var(--bg-input);
  color: var(--color-input);
  font-weight: 400;
  font-size: 16px;
  border: 0;
}

.content-input .content-input-name {
  position: relative;
}

.content-input .content-input-name img {
  position: absolute;
  left: 10px;
  bottom: 15px;
}
header .content-input select {
  width: 348px;
  height: 48px;
  padding: 12px 8px 12px 40px;
  gap: 12px;
  border-radius: 5px;
  color: var(--color-input);
  font-weight: 400;
  font-size: 16px;
  background-color: var(--bg-input);
  border: 0;
}

.content-input .content-input-city {
  position: relative;
}

.content-input .content-input-city img {
  position: absolute;
  left: 10px;
  bottom: 15px;
}
header .content-input button {
  background-color: var(--bg-content-input-button);
  width: 169px;
  height: 48px;
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--bg-content-input);
  border: 0;
}

header .image-1 img {
  position: absolute;
  top: 0px;
  left: 0px;
}

header .image-2 img {
  position: absolute;
  bottom: 0px;
  right: 0px;
}
</style>
