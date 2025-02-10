<template>
  <div class="parent">
    <div class="div1">Header</div>
    <div class="div2">Sidebar</div>
    <div class="div3">Main Content</div>
    <div class="div4">Footer</div>
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
  grid-column-gap: 10px;
  grid-row-gap: 10px;
  width: 100%;
  height: 100vh;
  padding: 10px;
  box-sizing: border-box;
}

.div1 {
  grid-area: 1 / 2 / 2 / 11;
  background-color: #ffcc00;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  background-color: #ff5733;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: white;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  background-color: #33ff57;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: white;
}

.div4 {
  grid-area: 5 / 8 / 6 / 13;
  background-color: #3366ff;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  color: white;
}
</style>
