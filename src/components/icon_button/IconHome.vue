<template>
  <div
    @mousedown="changeIcon('normal')"
    @mouseup="changeIcon('active')"
  >
    <component :is="iconType"></component>
    <span>首頁</span>
  </div>
</template>

<script>
import IconHome from '@/assets/icon/icon-home.svg'
import IconHomeActive from '@/assets/icon/icon-home-active.svg'

export default {
  name: 'IconHome',
  components: {
    normal: {
      template: '<IconHome/>'
    },
    active: {
      template: '<IconHomeActive/>'
    }
  },
  data: () => ({
    iconType: 'normal'
  }),
  methods: {
    changeIcon: function(type) {
      this.iconType = type
    }
  }
}
</script>
