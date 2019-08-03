<template>
  <div class="button-box">
    <PreviousNormal v-show="!isActive" />
  </div>
</template>

<script>
import PreviousNormal from '../../assets/icon/functions-previous.svg'

export default {
  name: 'button-previous',
  props: {
    isActive: Boolean
  },
  components: {
    PreviousNormal
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
