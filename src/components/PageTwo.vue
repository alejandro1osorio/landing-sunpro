<template>
  <div class="page-grid">
    <h1 class="page-title">Antiarrugas <strong style="border-bottom: 5px solid orange;">con Q10</strong></h1>

    <div class="title-image-container">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Imagen descriptiva" class="title-image"/>
    </div>

    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <!-- Imagen en el centro -->
      <div class="image-container">
        <div class="container-item">
          <div class="box top-left" style="flex-direction: row;">
            <p style="text-align: end;">Antioxidante <strong style="color: gray;">•</strong> <br> Antienvejecimiento <strong style="color: gray;">•</strong> <br> <strong>Estimula la producción de colágeno <strong style="color: gray;">•</strong></strong></p>
            <img src="../assets/beneficios-productos/icon7.png" alt="Hidrosense" style="transform: translate(4%, -17%) scale(1.53);" />
            <span class="line right"></span>
          </div>
          <!-- Contenedor inferior izquierdo -->
          <div class="box bottom-left" style="flex-direction: row;">
            <p>Complejo de Vitamina E. Para <strong>pieles sensibles</strong></p>
            <img src="../assets/beneficios-productos/icon8.png" alt="Algodón" style="transform: translate(8%, -18%) scale(1.51);" />
            <span class="line right"></span>
          </div>
        </div>
        
        <img src="../assets/productos/producto2.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 6%;"/>
        
        <div>
          <div class="box top-right">
            <img src="../assets/beneficios-productos/icon9.png" alt="Sin Parabenos" style="transform: translate(-2%, -18%) scale(1.51);" />
            <p style="font-size: 0.7rem;"><strong>Mezcla eficaz de filtros solares</strong> que proporcionan protección frente a diferentes tipos de radiación.</p>
            <span class="line left"></span>
          </div>
          <!-- Contenedor inferior derecho -->
          <div class="box bottom-right" style="height: 98px;">
            <img src="../assets/beneficios-productos/icon10.png" alt="No irrita ojos" style="transform: translate(-1%, -20%) scale(1.51);" />
            <p><strong style="color: gray;">•</strong> Anitoxidante. <br> <strong style="color: gray;">•</strong> <strong>Antienvejecimiento.</strong> <br> <strong style="color: gray;">•</strong> Hidratante. <br> <strong style="color: gray;">•</strong> Protección contra radiación UV. </p>
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
    <div v-if="activeTab" class="content-tab">
      <div class="tab-header">
        <button class="close-btn" @click="closeTab">
          <svg class="icon" width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 18L18 6M6 6L18 18" stroke="#214F79" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>

      <p v-if="activeTab === 'benefits'" class="text-tab">
        Con coenzima Q10, con antioxidantes, con hidratantes, resistente al agua.
      </p>
      <p v-if="activeTab === 'usage'">Agite antes de usar. Aplicar uniformemente sobre la piel. Esperar 15 minutos antes de exponerse al sol.  Reaplicar cada 2 horas o después de un tiempo prolongado en el sol o de mucha transpiración. Usar diariamente.</p>
      <p v-if="activeTab === 'composition'">Aqua (Water), Ethylhexyl Methoxycinnamate, Benzophenone-3, Bis-Ethylhexyloxyphenol Methoxyphenyl Triazine / Polymethylmethacrylate, Ethylhexyl Salicylate, Isocetyl Stearoyl Stearate / Phenethyl Benzoate / Titanium Dioxide, Dibutyl Adipate, Potassium Cetyl Phosphate, Ethylhexyl Triazone, Aqua (Water) / Hydrolyzed Wheat Protein / PVP Crosspolymer, Bis-Ethylhexyloxyphenol Methoxyphenyl Triazine, Dicaprylyl Carbonate, Polyamide-5, Glyceryl Stearate / Laureth-23, Benzyl Alcohol / Caprylyl Glycol, Isododecane / Dimethicone / Bis Isobutyl PPG 20 Crosspolymer, Propylheptyl Caprylate , VP / Hexadecene Copolymer, Glyceryl Stearate / Cetearyl Alcohol / Sodium Stearoyl Lactylate, Acrylic Acid / VP Crosspolymer, Physalis Angulata Extract / Caprylic / Capric Triglyceride, Propylene Glycol, Phospholipids / Ubiquinone / Caprylic / Capric Triglyceride / Isopropyl Myristate / BHT / Aqua (Water), Disodium Lauriminodipropionate Tocopheryl Phosphates, Parfum (Fragrance), Sodium Hydroxide, Panthenol, Silica, Pentaerythrityl Tetra-di-t-Butyl Hydroxyhydrocinnamate, Tetrasodium EDTA.</p>
    </div>

    <footer>
      <p class="text-footer"><strong>Mayor</strong> protección y resistente al agua</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'PageOne',
  data() {
    return {
      activeTab: '',
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
    closeTab() {
      this.activeTab = '';
    }
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
  background-color: #BCBCBC;
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
  background-color: #BCBCBC;
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

.tab-header {
  display: flex;
  justify-content: flex-end;
  padding: 5px;
}
.close-btn {
  background: transparent;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #EE8C67;
}

footer {
  background: #BCBCBC; 
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