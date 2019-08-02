<template>
  <div class="sidebar-button">
    <button-home :isActive="buttonState[0]" @click.native="changeState(0)" />
    <button-favorite :isActive="buttonState[1]" @click.native="changeState(1)"/>
    <button-list :isActive="buttonState[2]" @click.native="changeState(2)"/>
    <button-setting :isActive="buttonState[3]" @click.native="changeState(3)"/>
  </div>
</template>

<script>
import ButtonHome from './icon-button/ButtonHome'
import ButtonFavorite from './icon-button/ButtonFavorite'
import ButtonList from './icon-button/ButtonList'
import ButtonSetting from './icon-button/ButtonSetting'

export default {
  name: 'sidebar-area',
  components: {
    ButtonHome,
    ButtonFavorite,
    ButtonList,
    ButtonSetting
  },
  data: () => ({
    activeNow: 0,
    buttonState: [true, false, false, false]
  }),
  methods: {
    changeState: function(index) {
      console.log(index);
      this.buttonState[this.activeNow] = false
      this.buttonState[index] = true
      this.activeNow = index
      console.log(this.activeNow,this.buttonState)
    }
  }
}
</script>

<style>
.sidebar-button {
  background-color: darkslategrey;
}
</style>
