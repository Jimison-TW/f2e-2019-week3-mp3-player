<template>
  <div id="middle-page">
    <middle-header />
    <div class="tape">
      <img src="../assets/images/tape-big.png" alt="圖片消失" />
      <div id="progressContainer">
        <div id="myProgress">
          <div id="myBar"></div>
        </div>
        <span>00:00</span>
      </div>
      <radio-tap-area class="radio-tap" />
    </div>
  </div>
</template>

<script>
import MiddleHeader from '../components/MiddleHeader'
import RadioTapArea from './RadioTapArea'

export default {
  name: 'middle-page',
  components: {
    MiddleHeader,
    RadioTapArea
  }
}
</script>

<style scoped>
img {
  width: auto;
  height: auto;
  max-width: 100%;
  max-height: 100%;
}

#middle-page {
  width: 70%;
  height: 100%;
  background-color: darkslategrey;
}

.tape {
  text-align: center;
}

#myProgress {
  margin-top: 30px;
  margin-bottom: 50px;
  margin-left: 0px;
  margin-right: 0px;
  margin: auto;
  width: 90%;
  background-color: grey;
  border-radius: 10px;
}

#myBar {
  width: 20%;
  height: 20px;
  background-color: green;
  border-radius: 10px;
}

#progressContainer{
  height: 100px;
}
</style>
