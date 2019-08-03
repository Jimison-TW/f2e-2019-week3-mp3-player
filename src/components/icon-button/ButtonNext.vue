<template>
  <div class="button-box">
    <NextNormal v-show="!isActive" />
  </div>
</template>

<script>
import NextNormal from '../../assets/icon/functions-next.svg'

export default {
  name: 'button-next',
  props: {
    isActive: Boolean
  },
  components: {
    NextNormal
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
