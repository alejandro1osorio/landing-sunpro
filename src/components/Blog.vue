<template>
  <div class="blog-container" id="contenido-cientifico">
    <h1>Artículos Recientes</h1>
    <div class="article-container">
      <div class="article">
        <img :src="article.image" alt="Imagen del artículo" class="article-image" />
        <h2>{{ article.title }}</h2>
        <p>{{ article.description }}</p>
        <a :href="article.link" target="_blank" class="view-more">Ver más</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Blog",
  data() {
    return {
      article: {
        id: 1,
        title: "Sun and Skin",
        description: "People enjoy the sun. Some have even worshiped it. Sunlight is essential to many living things. But sunlight also has a dangerous side. It can harm your skin and even your eyes. The good news is you can take some simple steps to protect your body from sun damage and still enjoy the sun’s healthful effects.",
        image: "https://images.unsplash.com/photo-1740695400131-fe8001c68f1d?q=80&w=1978&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        link: "https://drive.google.com/file/d/1z2vZSLSobf91pQuajYLSxddnNNjGxl40/view?usp=sharing"
      }
    };
  },
};
</script>

<style scoped>
.blog-container {
  text-align: center;
  padding: 20px;
}

h1 {
  font-size: 2.5em;
  color: #2c3e50;
  margin-bottom: 30px;
}

.article-container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
}

.article {
  background-color: #f9f9f9;
  border-radius: 8px;
  width: 90%;
  max-width: 600px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  overflow: hidden;
  padding-bottom: 20px;
}

.article-image {
  width: 100%;
  height: auto;
  border-radius: 8px 8px 0 0;
}

h2 {
  font-size: 1.5em;
  margin: 10px 0;
  color: #34495e;
}

p {
  font-size: 1em;
  color: #7f8c8d;
  margin: 10px 20px;
  text-align: justify;
}

.view-more {
  text-decoration: none;
  color: #3498db;
  font-weight: bold;
  transition: color 0.3s;
}

.view-more:hover {
  color: #1d6fa5;
}
</style>
