<template>
  <div class="container">
    <h1 class="title">Radiación infrarroja - IR</h1>
    <div class="grid">
      <div class="left">
        <p class="text">
          Parte de la energía solar se transmite y se siente en forma de calor.<sup>1</sup> 
          Por tanto, cuando la piel se expone a IR, su temperatura puede aumentar hasta 40°C, 
          lo que genera fotoenvejecimiento, pigmentación y eritema.<sup>1</sup>
        </p>
      </div>
      <div class="right">
        <img src="../assets/otros/electromagnetic.png" alt="Imagen de ejemplo">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Radiacion",
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
}

html, body {
  width: 100%;
  overflow-x: hidden;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
  color: #244E75; 
}

.title {
  font-size: 36px; 
  font-weight: bold;
  margin-bottom: 20px;
}

.grid {
  display: grid;
  grid-template-columns: 1fr 1fr; 
  gap: 20px;
  align-items: center;
  justify-content: center;
  width: 100%;
}

.left, .right {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 200px;
  /* border: 2px solid #000000; */
  padding: 20px;
  /* background-color: #f9f9f92f; */
  text-align: center;
  width: 100%; 
  max-width: 100%; 
}

.left .text {
  font-size: 20px; 
  line-height: 1.6;
}

.right img {
  max-width: 100%;
  height: auto;
  display: block;
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr; 
    justify-items: center; 
    width: 100%;
  }

  .left, .right {
    width: 90%; 
    max-width: 400px; 
  }

  .title {
    font-size: 30px; 
  }

  .left .text {
    font-size: 20px; 
    text-align: start;
  }

  .right img {
    width: 150%; 
    max-width: 600px; 
  }
}
</style>
