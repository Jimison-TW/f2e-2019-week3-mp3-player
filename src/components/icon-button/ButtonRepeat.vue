<template>
  <div class="button-box">
    <RepeatNormal v-show="!isActive" />
    <RepeatActive v-show="isActive" />
  </div>
</template>

<script>
import RepeatNormal from '../../assets/icon/functions-repeat.svg'
import RepeatActive from '../../assets/icon/functions-repeat-active.svg'

export default {
  name: 'button-repeat',
  props: {
    isActive: Boolean
  },
  components: {
    RepeatNormal,
    RepeatActive
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
