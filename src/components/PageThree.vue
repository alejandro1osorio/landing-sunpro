<template>
  <div class="page-grid">
    <InfoThree />
    <h1 class="page-title">Textura <strong style="border-bottom: 5px solid orange;">Ultraligera</strong></h1>

    <div class="title-image-container">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Imagen descriptiva" class="title-image"/>
    </div>

    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <!-- Imagen en el centro -->
      <div class="image-container">
        <div class="container-item">
          <div class="box top-left" style="flex-direction: row;">
            <p>Con <strong>Hidrosense</strong> (Mezcla única de Jojoba + Biolípido de origen natural en nuestro portafolio)</p>
            <img src="../assets/beneficios-productos/icon11.png" alt="Hidrosense" style="transform: translate(5%, -20%) scale(1.54);" />
            <span class="line right"></span>
          </div>
          <!-- Contenedor inferior izquierdo -->
          <div class="box bottom-left" style="flex-direction: row;">
            <p>Con tela <strong>100% libre de plástico.</strong> Fibras naturales.</p>
            <img src="../assets/beneficios-productos/icon12.png" alt="Algodón" style="transform: translate(-2%, -20%) scale(1.54);" />
            <span class="line right"></span>
          </div>
        </div>
        
        <img src="../assets/productos/producto3.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 18%;"/>
        
        <div class="container-item">
          <div class="box top-right">
            <img src="../assets/beneficios-productos/icon13.png" alt="Sin Parabenos" style="transform: translate(-6%, -20%) scale(1.54);" />
            <p style="font-size: 0.7rem;">Sin Alcohol, parabenos, siliconas, colorante y sulfatos.</p>
            <span class="line left"></span>
          </div>
          <!-- Contenedor inferior derecho -->
          <div class="box bottom-right">
            <img src="../assets/beneficios-productos/icon14.png" alt="No irrita ojos" style="transform: translate(-6%, -20%) scale(1.54);" />
            <p style="font-size: 11px;"><strong>Con estudio de sensibilización e irritación dérmica.</strong> Aprobado y recomendado por pediatras y dermatólogos.</p>
            <span class="line left"></span>
          </div>
        </div>
      </div>
      <!-- Contenedor superior derecho -->

    </div>

    <div class="button-group">
      <button @click="setActiveTab('benefits')">Beneficios</button>
      <button @click="setActiveTab('usage')">Modo de uso</button>
      <button @click="setActiveTab('composition')">Composición</button>
    </div>
    <div class="content-tab">
      <p v-if="activeTab === 'benefits'" class="text-tab">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptate, voluptatibus!
      </p>
      <p v-if="activeTab === 'usage'">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis, dignissimos.</p>
      <p v-if="activeTab === 'composition'">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, obcaecati?</p>
    </div>

    <footer>
      <p class="text-footer">Apto para <strong>pieles grasas</strong></p>
    </footer>
  </div>
</template>

<script>
import InfoThree from './InfoThree.vue';

export default {
  name: 'PageOne',
  components: { InfoThree },
  data() {
    return {
      activeTab: 'benefits',
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style scoped>
.page-grid {
  display: grid;
  grid-template-rows: auto 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  height: 100%;
  /* padding: 20px; */
  box-sizing: border-box;
  /* gap: 20px; */
}

.page-title {
  font-size: 1.8rem;
  font-weight: 300;
  text-align: center;
  color: #214F79;
}

.title-image-container {
  display: flex;
  justify-content: center;
  margin: 10px 0;
}

.title-image {
  max-width: 55%;
  height: auto;
}

.image-structure {
  display: grid;
  grid-template-areas:
    "top-left image top-right"
    "bottom-left image bottom-right";
  /* grid-template-columns: auto 1fr auto; */
  grid-template-columns: 1fr 0.4fr 1fr;
  grid-template-rows: auto auto;
  gap: 20px;
  align-items: center;
  justify-items: center;
  width: 100%;
}

.image-container {
  grid-area: image;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 130%;
  max-width: 300px;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  /* box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); */
}

.box {
  display: flex;
  align-items: center;
  width: 280px; /* Aumentado el ancho de los contenedores */
  height: auto;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  gap: 8px; /* Ajustado el espaciado */
  /* padding: 8px; */
  position: relative; /* Necesario para las líneas */
}

.box img {
  max-width: 100px; /* Disminuido el tamaño de las imágenes */
  height: auto;
}

.box p {
  font-weight: 500;
  color: #214F79;
  font-size: 0.8rem; /* Reducido el tamaño del texto */
}

/* Líneas decorativas */
.line {
  position: absolute;
  width: 100px;
  height: 2px;
  background-color: #7BA0AD;
  top: 50%;
  transform: translateY(-50%);
}

.line.right {
  right: -94px;
}

.line.left {
  left: -94px;
}

.line::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: #7AA0AD;
  border: 2px solid #CFE1ED;
  border-radius: 50%;
  top: 50%;
  transform: translateY(-50%);
}

.line.right::after {
  right: -10px;
}

.line.left::after {
  left: -10px;
}

.top-left {
  grid-area: top-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 57px 59px 59px 17px;
  margin-bottom: 50%;
}

.bottom-left {
  grid-area: bottom-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 57px 59px 59px 17px;
}

.top-right {
  grid-area: top-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 100px 100px 35px 100px;
  margin-bottom: 50%;
}

.bottom-right {
  grid-area: bottom-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 100px 100px 35px 100px;
}

.content-tab {
  border: 2px solid orange;
  border-radius: 0px 12px 12px 12px;
  width: 60%;
  padding: 20px;
  background: #F3F3F3;
}

.content-tab, p {
  font-weight: 400;
  color: #214F79;
}

.button-group {
  display: flex;
  gap: 10px;
}

button {
  padding: 5px 10px;
  font-size: 0.9rem;
  border: none;
  border-radius: 5px;
  background-color: #DEE5E7;
  color: #214F79;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  color: white;
  background-color: orange;
}

button:active,
button:focus {
  background-color: orange;
  color: #fff;
}


footer {
  background: #EE8C67; 
  font-size: 1.5rem;
  width: 100%; 
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text-footer {
  color: #fff;
}

@media (max-width: 768px) {
  .title-image {
    max-width: 80%;
  }
  .box {
    visibility: hidden;
  }

  .content-tab, p {
    font-size: 0.9rem;
  }
}
</style>