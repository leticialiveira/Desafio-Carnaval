<script setup>
    
</script>

<template>
  <div class="title">
    <p>Blocos recomendados</p>
    <div class="button-select">
      <button>LISTA</button>
      <button>MAPA</button>
    </div>
  </div>
  <div class="grid-cards">
    <article>
      <img src="../assets/img/vovopython.png" alt="" />
      <header>
        <h1>O Python do vovô não sobe mais</h1>
        <p>
          Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet
          sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>São Paulo - SP</p>
      </footer>
    </article>

    <article>
      <img src="../assets/img/null.png" alt="" />
      <header>
        <h1>Todo mundo null</h1>
        <p>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>Florianópolis - SC</p>
      </footer>
    </article>

    <article>
      <img src="../assets/img/exception.png" alt="" />
      <header>
        <h1>Hoje dou exception</h1>
        <p>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>Curitiba - PR</p>
      </footer>
    </article>
  </div>

  <div class="grid-cards">
    <article>
      <img src="../assets/img/node.png" alt="" />
      <header>
        <h1>Manda Node</h1>
        <p>
          Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet
          sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>Salvador - BA</p>
      </footer>
    </article>

    <article>
      <img src="../assets/img/back-end.png" alt="" />
      <header>
        <h1>Só no back-end</h1>
        <p>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>São Paulo - SP</p>
      </footer>
    </article>

    <article>
      <img src="../assets/img/ruby.png" alt="" />
      <header>
        <h1>Esse anel não é de Ruby</h1>
        <p>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>São Paulo - SP</p>
      </footer>
    </article>
  </div>

  <div class="grid-cards">
    <article>
      <img src="../assets/img/pimenta.png" alt="" />
      <header>
        <h1>Pimenta no C# dos outros é refresco</h1>
        <p>
          Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet
          sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>Rio de Janeiro - RJ</p>
      </footer>
    </article>

    <article>
      <img src="../assets/img/cache.png" alt="" />
      <header>
        <h1>EnCACHE aqui</h1>
        <p>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>Porto Alegre - RS</p>
      </footer>
    </article>

    <article>
      <img src="../assets/img/Java.png" alt="" />
      <header>
        <h1>Não valho nada mas JAVA li</h1>
        <p>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.
        </p>
      </header>
      <footer>
        <img src="../assets/icons/Vector (2).png" alt="icon endereço" />
        <p>São Paulo - SP</p>
      </footer>
    </article>
  </div>
</template>

<style scoped>
.title {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-bottom: 50px;
}

.title p {
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

.grid-cards {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

article {
  background-color: var(--bg-article);
  width: 384px;
  height: 323px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 30px;
  margin-bottom: 40px;
  border: 1px solid var(--border-article);
  border-radius: 10px;
}

article img {
    border-radius: 2%;
}
article header {
    padding-left: 15px;
}
article header h1 {
    color: var(--color-article-h1);
    font-weight: 700;
    font-size: 20px;
    padding-bottom: 10px;
}

article header p {
  color: var(--color-article-p);
  font-weight: 400;
  font-size: 16px;
}

article footer {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
}

article footer img {
    position: absolute;
    left: 15px;

}

article footer p {
    font-weight: 400;
    font-size: 16px;
    color: var(--color-article-p);
    padding-left: 40px;
    
}

article:hover {
    transform: scale(1.1);
}
</style>
