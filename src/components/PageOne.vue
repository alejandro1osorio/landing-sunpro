<template>
  <div class="page-grid">
    <h1 class="page-title">Textura ligera <strong>con <strong style="border-bottom: 5px solid orange;">Color</strong></strong></h1>

    <div class="title-image-container">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Imagen descriptiva" class="title-image"/>
    </div>

    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <!-- Imagen en el centro -->
      <div class="image-container">
        <div class="container-item">
          <div class="box top-left" style="flex-direction: row;">
            <p><strong>Physavie 250</strong> Calmante y para pieles sensibles.</p>
            <img src="../assets/beneficios-productos/icon1.png" alt="Hidrosense" style="transform: translate(2%, -2%) scale(1.29);" />
            <span class="line right"></span>
          </div>

          <div class="box top-left" style="flex-direction: row;">
            <p><strong>Coenzima Q10</strong> Protección del daño por radiación UV, Antienvejecimiento e hidratante.</p>
            <img src="../assets/beneficios-productos/icon2.png" alt="Hidrosense" style="transform: translate(2%, -2%) scale(1.30);" />
            <span class="line right"></span>
          </div>

          <!-- Contenedor inferior izquierdo -->
          <div class="box bottom-left" style="flex-direction: row;">
            <p><strong>Provitamina B5</strong> Hidratante, alivia diversas molestias en la piel y mejora su apariencia.</p>
            <img src="../assets/beneficios-productos/icon3.png" alt="Algodón" style="transform: translate(2%, 0%) scale(1.30);" />
            <span class="line right"></span>
          </div>
        </div>
        
        <img src="../assets/productos/producto1.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 26px;"/>
        
        <div>
          <div class="box top-right">
            <img src="../assets/beneficios-productos/icon4.png" alt="Sin Parabenos" style="transform: translate(-2%, 0%) scale(1.36);" />
            <p style="font-size: 0.7rem;"><strong>Niacinamida</strong> Reduce el enrojecimiento, manchas, mejora la función barrera de la piel y previene la aparición de arrugas.</p>
            <span class="line left"></span>
          </div>

          <div class="box top-right">
            <img src="../assets/beneficios-productos/icon5.png" alt="Sin Parabenos" style="transform: translate(1%, -1%) scale(1.30);" />
            <p style="font-size: 0.7rem;"><strong>Lumiskim</strong> Antioxidante, antipolución y reduce manchas.</p>
            <span class="line left"></span>
          </div>

          <!-- Contenedor inferior derecho -->
          <div class="box bottom-right">
            <img src="../assets/beneficios-productos/icon6.png" alt="No irrita ojos" style="transform: translate(3%, 5%) scale(1.30);" />
            <p><strong>Vitamina E</strong> Retardo del envejecimiento de las células de la piel y antioxidante.</p>
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
        Unifica el tono de la piel, se adapta a diferentes fototipos de piel, textura ligera, sin sensación grasosa, reduce la producción de sebo y el tamaño de los poros, anti-polución, efecto aclarante progresivo.
      </p>
      <p v-if="activeTab === 'usage'">Agite antes de usar. Aplicar uniformemente sobre la piel. Esperar 15 minutos antes de exponerse al sol.  Reaplicar cada 2 horas o después de un tiempo prolongado en el sol o de mucha transpiración. Usar diariamente.</p>
      <p v-if="activeTab === 'composition'">Aqua (Water), Ethylhexyl Methoxycinnamate, Ethylhexyl Salicylate, Homosalate, Diethylamino Hydroxybenzoyl Hexyl Benzoate, Silica, Dibutyl Adipate, Octocrylene, Aqua (Water) / Hydrolyzed Wheat Protein / PVP Crosspolymer, Brassica Campestris / Aleurites Fordi Oil Copolymer , Glycerin, Niacinamide, Pentaerythrityl Distearate, Silica, Titanium Dioxide / PEG-12 Dimethicone, VP / Hexadecene Copolymer, Sodium Stearoyl Glutamate, CI 77492 (and) C.I 77491 (and) C.I. 77499 (and) Ethylhexyl Methoxycinnamate, Caprylic / Capric Triglyceride / Diacetyl Boldine, Benzyl Alcohol / Caprylyl Glycol, Isododecane / Dimethicone / Bis Isobutyl PPG 20 Crosspolymer, Glyceryl Stearate / Cetearyl Alcohol / Sodium Stearoyl Lactylate, Physalis Angulata Extract / Caprylic / Capric Triglyceride, Sodium Polyacrylate, Magnesium Sulfate, Phospholipids / Ubiquinone / Caprylic / Capric Triglyceride / Isopropyl Myristate / BHT / Aqua (Water), Xanthan Gum, Pentaerythrityl Tetra-di-t-Butyl Hydroxyhydrocinnamate, Tetrasodium EDTA, Tocopheryl Acetate, Panthenol, Citric Acid. </p>
    </div>

    <footer>
      <p class="text-footer">Un solo tono se adapta de los <strong>fototipos II al IV</strong></p>
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
/* .info-container {
  text-align: center;
  padding: 10px;
  border-radius: 10px;
  margin-bottom: 10px;
} */

.page-grid {
  display: grid;
  grid-template-rows: auto 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  height: 100%;
  /* padding: 0 20px; */
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
  width: 94px;
  height: 2px;
  background-color: #EFCBB5;
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
  background-color: #EFCBB5;
  border: 2px solid #ee9a66;
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
  margin-bottom: 15%;
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
  margin-bottom: 15%;
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
  background: #EFCBB5; 
  font-size: 1.5rem;
  width: 100%; 
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text-footer {
  color: #214F79;
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