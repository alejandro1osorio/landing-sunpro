<template>
  <div class="container">
    <h1 class="title">La radiación solar y la luz artificial <br> <strong style="color: orange;">tienen diferentes impactos en la piel</strong></h1>
    
    <div class="content">
      <!-- Contenedor izquierdo -->
      <div class="left-container">

        <div class="item main-item">
          <h2>Rayos UV</h2>
          <p>Los rayos UV son el factor de riesgo modificable más importante para el cáncer de piel.<sup>2</sup></p>
        </div>

        <div class="item" v-for="(item, index) in items" :key="index">
          <div class="number">{{ item.number }}</div>
          <div class="text">
            <h3>{{ item.title }}</h3>
            <p>{{ item.description }}<sup v-if="item.sup">{{ item.sup }}</sup></p> 
          </div>
        </div>
      </div>

      <!-- Contenedor derecho con imagen -->
      <div class="right-container">
        <img src="../assets/otros/capas.png" alt="Esquema de piel" class="image"/>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { number: "1", title: "Radiación UVB", description: "Alrededor del 70% de la radiación UVB es absorbida por el estrato córneo.", sup: "1,2" },
        { number: "2", title: "Radiación UVA", description: "Los rayos UVA son en gran medida responsables del fotoenvejecimiento provocado por la radiación.", sup: "1" },
        { number: "3", title: "Visible", description: "Provoca daños en la dermis: manchas, fotoenvejecimiento y cáncer cutáneo." },
        { number: "4", title: "IR-A", description: "Provoca daños en el ADN celular, causa fotoenvejecimiento y altera la síntesis de colágeno." }
      ]
    };
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  box-sizing: border-box;
  color: #244E75;
}

.title {
  text-align: center;
  font-size: 1.8rem;
  margin-bottom: 20px;
  line-height: 1.2;
  font-weight: 400;
}

.content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  align-items: center;
}

.left-container {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.main-item {
  color: rgb(0, 0, 0);
  text-align: left; 
  display: flex;
  flex-direction: column; 
  align-items: flex-start; 
  color: #244E75;
}

.main-item h2 {
  margin: 0;
  font-size: 1.5rem; 
  font-weight: bold;
  text-align: left !important; 
  width: 100%; 
}

.item {
  display: flex;
  align-items: center;
  /* background: #f5f5f5b2; */
  border-radius: 10px;
}

.number {
  font-size: 1.3rem;
  font-weight: bold;
  background: orange;
  color: white;
  width: 32px;
  height: 32px;
  min-width: 32px;
  min-height: 32px;
  aspect-ratio: 1/1;  
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  margin-right: 15px;
  align-self: start;
}

.text h3 {
  margin: 0;
  font-size: 1.2rem;
}

.text p {
  margin: 5px 0 0;
  font-size: 1rem;
}

.right-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

@media (max-width: 768px) {
  .title {
    font-size: 1.2rem;
  }

  .content {
    grid-template-columns: 1fr;
  }
}
</style>
