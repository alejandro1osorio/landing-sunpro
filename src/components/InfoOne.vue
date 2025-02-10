<template>
  <div class="parent">
    <div class="div1"><h1 class="title">Protector Solar con Color <strong>SPF50</strong></h1></div>
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
}

.div1 {
  grid-area: 1 / 2 / 2 / 11;
  background-color: #ff5733;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  /* height: 50px; */
  margin: 0;
}

.div1 .title {
  font-size: 1.5em;
  font-weight: 300;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  /* background-color: #33a1ff; */
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  margin: 0;
}

.div2 .image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  /* background-color: #33ff57; */
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
  /* background-color: #ff33a1; */
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 80px;
  margin: 0;
}

.div4 .image-centered {
  max-width: 120%;
  max-height: 120%;
  object-fit: contain;
}
</style>
