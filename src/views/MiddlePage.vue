<template>
  <div id="middle-page">
    <middle-header />
    <div class="tape">
      <img src="../assets/images/tape-big.png" alt="圖片消失" />
      <volume-slider />
      <radio-tap-area />
    </div>
  </div>
</template>

<script>
import MiddleHeader from '../components/MiddleHeader'
import RadioTapArea from './RadioTapArea'
import VolumeSlider from '../components/VolumeSlider'

export default {
  name: 'middle-page',
  components: {
    MiddleHeader,
    RadioTapArea,
    VolumeSlider
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
</style>
