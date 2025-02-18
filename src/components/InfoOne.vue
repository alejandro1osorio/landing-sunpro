<template>
  <div class="parent">
    <div class="div1">
      <div class="top-line"></div>
      <h1 class="title">Protector Solar con Color <strong>SPF50</strong></h1>
    </div>
    <div class="div2">
      <img src="../assets/otros/baby2.png" alt="Placeholder Image" class="image" />
    </div>
    <div class="div3">
      <img src="../assets/otros/info1.png" alt="Placeholder Image" class="image-centered" />
    </div>
    <div class="div4">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Placeholder Image" class="image-centered" />
    </div>
  </div>
</template>

<script>
export default {
  name: "GridLayout"
};
</script>

<style scoped>
.parent {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  width: 100%;
  height: 100vh;
  padding: 0;
  box-sizing: border-box;
  /* background-color: #f4f4f4; */
}

.div1 {
  grid-area: 1 / 2 / 2 / 11;
  /* background-color: #ff58336c; */
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  /* height: 50px; */
  margin: 0;
}

.div1 .top-line {
  position: absolute;
  top: 0;
  left: 50%;
  width: 20%;
  height: 5px;
  background-color: orange;
  transform: translateX(-70%);
}

.div1 .title {
  font-size: 2em;
  font-weight: 300;
  color: #214F79;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  /* background-color: #1b4f7c62; */
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  margin: 0;
}

.div2 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  /* background-color: #08531669; */
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 100%;
  margin: 0;
}

.div3 .image-centered {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.div4 {
  grid-area: 5 / 8 / 6 / 13;
  /* background-color: #5a2441a8; */
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 80px;
  margin: 0;
}

.div4 .image-centered {
  max-width: 140%;
  max-height: 140%;
  object-fit: contain;
}

@media screen and (min-width: 1400px) {
  /* Estilos para monitores muy grandes */
  .div4 {
    height: 130px;
  }
}

@media screen and (min-width: 1024px) and (max-width: 1399px) {
  /* portatiles con pantallas medianas */
  .div4 {
    height: 90px;
  }
}

@media screen and (max-width: 768px) {
  .parent {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    height: 110vh;
  }

  .div1 {
    grid-area: 1 / 1 / 2 / 7;
  }

  .div1 .title {
    font-size: 1.5em;
  }

  .div2 {
    grid-area: 2 / 1 / 3 / 7;
  }

  .div3 {
    grid-area: 3 / 1 / 4 / 7;
  }

  .div4 {
    grid-area: 4 / 1 / 5 / 7;
  }
}
</style>
