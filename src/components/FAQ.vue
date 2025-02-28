<template>
    <div class="faq-container">
      <h2 class="faq-title">
        Preguntas <span class="highlight">Frecuentes</span>
      </h2>
      <div class="faq-content">
        <div class="faq-image">
          <img src="../assets/otros/doctor.png" alt="Imagen relacionada" />
        </div>
        <div class="faq-accordion-container">
          <div class="faq-accordion">
            <div v-for="(question, index) in questions" :key="index" class="accordion-item">
              <button class="accordion-header" @click="toggle(index)">
                {{ question.title }}
                <span :class="{'rotate': activeIndex === index}" class="accordion-icon">+</span>
              </button>
              <div v-if="activeIndex === index" class="accordion-body">
                <p>{{ question.content }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bottom-line"></div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeIndex: null,
        questions: [
          {
            title: "¿Qué tipo de filtros solares tiene Sun Pro?",
            content: "Sun Pro maneja una mezcla de hasta 11 filtros diferentes por referencia, todos avalados por la regulación colombiana para el uso en la piel y tener una adecuada y alta protección solar, entre nuestros filtros puedes encontrar filtros orgánicos y filtro mineral.",
          },
          {
            title: "¿Sun Pro es apto para pieles sensibles?",
            content: "Para la mayoría de las patologías de la piel se recomienda complementar el tratamiento correspondiente con protección solar. Además, Sun Pro tiene referencias aptas para pieles sensibles y todos nuestros productos son hipoalergénicos y dermatológicamente comprobados.",
          },
          {
            title: "¿Sun Pro es de amplio espectro?",
            content: "Si, nuestros protectores solares faciales protegen de todos los rayos del espectro de la luz visible, incluyendo al luz azul natural o emitida por dispositivos electrónicos y luces led, además de la protección UVA, UVB e Infrarroja. ",
          },
          {
            title: "¿Qué beneficios adicionales tiene Sun Pro para el cuidado de la piel?",
            content: "Nuestros protectores solares cuentan con una mezcla de ingredientes activos que proporcionan diferentes beneficios para el cuidado de la piel como hidratación, antioxidantes, estimulo a la producción de colágeno y complejos de vitaminas. Además, nuestros protectores solares faciales cuentan con coenzima Q10 que es antiarrugas, antienvejecimiento, hidratante y protege contra la radiación UV.",
          },
          {
            title: "¿Los protectores solares Sun Pro son hipoalergénicos?",
            content: "Si, los protectores solares Sun Pro son hipoalergénicos y dermatológicamente comprobados",
          },
          {
            title: "¿Sun Pro es resistente al agua?",
            content: "Si, los protectores solares Sun Pro son resistentes al agua hasta por 80 minutos dependiendo de la referencia.",
          },
          {
            title: "¿Sun Pro es comedogénico?",
            content: "No, los protectores solares Sun Pro no obstruyen los poros ni favorecen la aparición de espinillas ni puntos negros.",
          },
          {
            title: "¿Qué estudios respaldan a Sun Pro?",
            content: "Contamos con estudios regulatorios y/o evaluaciones clínicas de factor de protección solar, rayos UVA, luz visible y luz azul, rayos IR-Antioxidante. Además, contamos con estudios, evaluaciones y/o ensayos clínicos que ratifican que nuestros productos son dermatológicamente comprobados, hipoalergénicos, no lágrimas, no comedogénicos, aptos para pieles sensibles y tolerancia ocular, dependiendo de la referencia. ",
          },
        ],
      };
    },
    methods: {
      toggle(index) {
        this.activeIndex = this.activeIndex === index ? null : index;
      },
    },
  };
  </script>
  
  <style scoped>
  .faq-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 20px;
    position: relative;
    padding-bottom: 10px;
  }
  
  .faq-title {
    text-align: center;
    font-size: 36px;
    /* font-family: "Arial", sans-serif; */
    color: #1F4F7A;
    margin-bottom: 20px;
    font-weight: 400;
  }
  
  .faq-title .highlight {
    color: #1F4F7A; /* Color para "Frecuentes" */
    font-weight: bold; /* Negrita para "Frecuentes" */
  }

  .faq-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    width: 100%;
  }
  
  .faq-image {
  display: flex; 
  justify-content: center; 
  align-items: center; 
}

  .faq-image img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 8px;
  }
  
  .faq-accordion-container {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }
  
  .faq-accordion {
    width: 90%;
  }
  
  .accordion-item {
    border: 1px solid #E6DED1;
    border-left-color: #e2cbb0;
    border-left-width: 10px;
    border-radius: 8px;
    margin-bottom: 10px;
    overflow: hidden;
  }
  
  .accordion-header {
    background: #E6DED1;
    color: #6F717B;
    padding: 15px;
    text-align: left;
    font-size: 18px;
    border: none;
    width: 100%;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .accordion-body {
    padding: 15px;
    background: #fff;
    font-size: 16px;
    /* font-family: "Arial", sans-serif; */

    line-height: 1.6;
    color: #444;
  }
  
  .accordion-icon {
    color: #F6A81D;
    font-size: 20px;
    font-weight: bold;
    transition: transform 0.3s;
  }
  
  .accordion-icon.rotate {
    transform: rotate(45deg);
  }

  .bottom-line {
    width: 50%; 
    height: 4px; 
    background-color: #AFD8EC; 
    border-radius: 2px;
    position: absolute;
    bottom: -14px; 
    left: 50%;
    transform: translateX(-50%);
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .faq-content {
        grid-template-columns: 1fr;
    }

    .accordion-header {
        font-size: 15px;
    }

    .accordion-body {
        font-size: 14px;
    }
  }
  </style>
  