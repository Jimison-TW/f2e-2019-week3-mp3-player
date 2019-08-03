<template>
  <div>
    <ListNormal v-show="!isActive" />
    <ListActive v-show="isActive" />
    <p :style="{ color: textColor }">清單</p>
  </div>
</template>

<script>
import ListNormal from '../../assets/icon/icon-like.svg'
import ListActive from '../../assets/icon/icon-like-active.svg'

export default {
  name: 'button-list',
  props: {
    isActive: Boolean
  },
  data: () => ({
    textColor: '#515151'
  }),
  components: {
    ListNormal,
    ListActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      this.textColor = newVal ? '#ffffff' : '#515151'
    }
  }
}
</script>
