<template>
  <div>
    <SettingNormal v-show="!isActive" />
    <SettingActive v-show="isActive" />
    <p :style="{ color: textColor }">設定</p>
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
  data: () => ({
    textColor: '#515151'
  }),
  components: {
    SettingNormal,
    SettingActive
  },
  watch: {
    isActive: function(newVal, oldVal) {
      this.textColor = newVal ? '#ffffff' : '#515151'
    }
  }
}
</script>
