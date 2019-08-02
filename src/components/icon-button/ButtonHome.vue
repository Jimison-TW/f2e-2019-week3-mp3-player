<template>
  <div>
    <HomeNormal v-show="!isActive" />
    <HomeActive v-show="isActive" />
    <p>首頁</p>
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
  data:()=>({
    
  }),
  components: {
    HomeNormal,
    HomeActive
  },
  watch: {
    '$props': {
      handler:function(val,oldVal){
        console.log('watch',val)
      },
      deep:true
    }
  }
}
</script>
