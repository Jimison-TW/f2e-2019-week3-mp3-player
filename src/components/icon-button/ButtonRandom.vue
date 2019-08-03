<template>
  <div class="button-box">
    <RandomNormal v-show="!isActive" />
    <RandomActive v-show="isActive" />
  </div>
</template>

<script>
import RandomNormal from '../../assets/icon/functions-random.svg'
import RandomActive from '../../assets/icon/functions-random-active.svg'

export default {
  name: 'button-random',
  props: {
    isActive: Boolean
  },
  components: {
    RandomNormal,
    RandomActive
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
