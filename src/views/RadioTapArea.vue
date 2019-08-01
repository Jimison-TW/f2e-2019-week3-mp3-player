<template>
  <div class="radio-container">
    <button class="button-box"></button>
    <button class="button-box"></button>
    <button class="button-box"></button>
    <button class="button-box"></button>
    <button class="button-box"></button>
  </div>
</template>

<script>
export default {
  name: 'radio-tap-area'
}
</script>

<style scoped>
.radio-container {
  width: 100%;
  height: 200px;
  background-color: cadetblue;
  display: flex;
  align-items: center;
  justify-content: center;
}

.button-box {
  width: 100px;
  height: 150px;
  background-color: #3A3A3A;
  margin-left: 5px;
  border-radius:10px
}
</style>
