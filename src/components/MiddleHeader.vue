<template>
  <div>
    <header class="header-style">
      <img src="../assets/images/img-1.jpg" alt="圖片失效" id="image" />
      <span>異鄉人樂團 The Strangers</span>
      <icon name="icon-tape" scale="100" />
    </header>
  </div>
</template>

<script>
export default {
  name: 'middle-header'
}
</script>

<style scoped>
img {
  width: 59px;
  height: 59px;
  border-radius: 50%;
  margin-left: 50px;
}

span {
  height: 100px;
  color: white;
  font-size: 20px;
}

.header-style {
  background-color: darkgreen;
}
</style>
