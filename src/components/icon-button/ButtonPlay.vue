<template>
  <div class="button-box">
    <PlayNormal v-show="!isActive" />
  </div>
</template>

<script>
import PlayNormal from '../../assets/icon/functions-play.svg'

export default {
  name: 'button-play',
  props: {
    isActive: Boolean
  },
  components: {
    PlayNormal
  }
}
</script>

<style scoped>
.button-box {
  width: 100px;
  height: 150px;
  background-color: #3a3a3a;
  margin-left: 5px;
  border-radius: 10px;
  line-height: 150px;
}
</style>
