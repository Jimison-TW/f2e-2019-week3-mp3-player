<template>
  <div>
    <SettingNormal v-show="!isActive" />
    <SettingActive v-show="isActive" />
    <p>設定</p>
  </div>
</template>

<script>
import SettingNormal from '../../assets/icon/icon-setting.svg'
import SettingActive from '../../assets/icon/icon-setting-active.svg'

export default {
  name: 'button-setting',
  props: {
    isActive: Boolean
  },
  components: {
    SettingNormal,
    SettingActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      console.log(newVal, oldVal)
    }
  }
}
</script>
