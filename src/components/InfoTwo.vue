<template>
  <div class="parent">
    <div class="div1">Header</div>
    <div class="div2">Sidebar</div>
    <div class="div3">Content</div>
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
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  width: 100%;
  height: 100vh;
  padding: 0;
  box-sizing: border-box;
  background-color: #f4f4f4;
}

.div1 {
  grid-area: 1 / 2 / 2 / 11;
  background-color: #ff5733;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 50px;
  margin: 0;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  background-color: #33a1ff;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 100%;
  margin: 0;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  background-color: #33ff57;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 100%;
  margin: 0;
}

.div4 {
  grid-area: 5 / 8 / 6 / 13;
  background-color: #ff33a1;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 80px;
  margin: 0;
}
</style>
