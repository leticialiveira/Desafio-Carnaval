<script setup>
    defineProps({
        image: String,
        title: String,
        description: String,
        address: String,
        link: String
    })

</script>

<template>    
    <article>
        <img :src='image' alt="" />
        <header>
            <a :href='link'>{{ title }}</a>
            <!-- <h1>{{ title }}</h1> -->
            <p>{{ description }}</p>
        </header>
        <footer>
            <img src="../assets/icons/Vector_gps.png" alt="icon endereço" />
            <p>{{ address }}</p>
        </footer>
    </article>
</template>

<style scoped>


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
article header a {
    color: var(--color-article-h1);
    font-weight: 700;
    font-size: 20px;
    padding-bottom: 10px;
    text-decoration: none;
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

