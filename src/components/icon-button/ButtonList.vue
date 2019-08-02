<template>
  <div>
    <ListNormal v-show="!isActive" />
    <ListActive v-show="isActive" />
    <p>清單</p>
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
  components: {
    ListNormal,
    ListActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      console.log(newVal, oldVal)
    }
  }
}
</script>
