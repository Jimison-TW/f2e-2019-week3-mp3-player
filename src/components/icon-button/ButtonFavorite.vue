<template>
  <div>
    <LikeNormal v-show="!isActive" />
    <LikeActive v-show="isActive" />
    <p :style="{ color: textColor }">最愛</p>
  </div>
</template>

<script>
import LikeNormal from '../../assets/icon/icon-like.svg'
import LikeActive from '../../assets/icon/icon-like-active.svg'

export default {
  name: 'button-like',
  props: {
    isActive: Boolean
  },
  data: () => ({
    textColor: '#515151'
  }),
  components: {
    LikeNormal,
    LikeActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      this.textColor = newVal ? '#ffffff' : '#515151'
    }
  }
}
</script>
