<template>
  <div class="container">
    <h1 class="title">La radiación solar y la luz artificial tienen diferentes impactos en la piel</h1>
    
    <div class="content">
      <!-- Contenedor izquierdo -->
      <div class="left-container">
        <div class="item" v-for="(item, index) in items" :key="index">
          <div class="number">{{ item.number }}</div>
          <div class="text">
            <h3>{{ item.title }}</h3>
            <p>{{ item.description }}</p>
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
        { number: "1", title: "Radiación UVB", description: "Alrededor del 70% de la radiación UVB es absorbida por el estrato córneo." },
        { number: "2", title: "Radiación UVA", description: "Los rayos UVA son en gran medida responsables del fotoenvejecimiento provocado por la radiación." },
        { number: "3", title: "Visible", description: "Provoca daños en la dermis: manchas, fotoenvejecimiento y cáncer cutáneo." },
        { number: "4", title: "IR-A", description: "Provoca daños en el ADN celular, causa fotoenvejecimiento y altera la síntesis de colágeno." }
      ]
    };
  }
};
</script>

<style scoped>
/* Estilos generales */
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  box-sizing: border-box;
}

/* Título centrado */
.title {
  text-align: center;
  font-size: 1.8rem;
  margin-bottom: 20px;
}

/* Diseño responsivo con Grid */
.content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
  align-items: center;
}

/* Contenedor izquierdo */
.left-container {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

/* Cada fila con información */
.item {
  display: flex;
  align-items: center;
  background: #f5f5f5;
  /* padding: 15px; */
  border-radius: 10px;
}

/* Número con estilo */
.number {
  font-size: 1.5rem;
  font-weight: bold;
  background: orange;
  color: white;
  width: 40px;
  height: 40px;
  min-width: 40px;
  min-height: 40px;
  aspect-ratio: 1/1;  /* 🔹 Asegura que siempre sea un círculo perfecto */
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  margin-right: 15px;
  align-self: start;
}

/* Texto de cada fila */
.text h3 {
  margin: 0;
  font-size: 1.2rem;
  color: #333;
}

.text p {
  margin: 5px 0 0;
  font-size: 1rem;
  color: #666;
}

/* Contenedor derecho */
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

/* Responsividad: En móviles los contenedores se apilan */
@media (max-width: 768px) {
  .content {
    grid-template-columns: 1fr;
  }
}
</style>
