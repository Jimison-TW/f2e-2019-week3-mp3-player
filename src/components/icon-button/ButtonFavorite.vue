<template>
  <div>
    <LikeNormal v-show="!isActive" />
    <LikeActive v-show="isActive" />
    <p>最愛</p>
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
  components: {
    LikeNormal,
    LikeActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      console.log(newVal, oldVal)
    }
  }
}
</script>
