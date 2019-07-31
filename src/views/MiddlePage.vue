<template>
  <div id="middle-page">
    <middle-header />
    <div class="tape">
      <img src="../assets/images/tape-big.png" alt="圖片消失" />
    </div>
  </div>
</template>

<script>
import MiddleHeader from '../components/MiddleHeader'

export default {
  name: 'middle-page',
  components: {
    MiddleHeader
  }
}
</script>

<style>
#middle-page {
  width: 70%;
  height: 100%;
  background-color: darkslategrey;
}

.tape {
  text-align: center;
}
</style>
