<template>
  <div>
    <HomeNormal v-show="!isActive" />
    <HomeActive v-show="isActive" />
    <p :style="{ color: textColor }">首頁</p>
  </div>
</template>

<script>
import HomeNormal from '../../assets/icon/icon-home.svg'
import HomeActive from '../../assets/icon/icon-home-active.svg'

export default {
  name: 'button-home',
  props: {
    isActive: Boolean
  },
  data: () => ({
    textColor: '#ffffff'
  }),
  components: {
    HomeNormal,
    HomeActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      this.textColor = newVal ? '#ffffff' : '#515151'
    }
  }
}
</script>
