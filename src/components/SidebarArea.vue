<template>
  <div class="sidebar-button">
    <router-link to="/">
      <button-home :isActive="homeButtonState" @click.native="onClick(0)" />
    </router-link>
    <router-link to="/about">
      <button-favorite :isActive="likeButtonState" @click.native="onClick(1)" />
    </router-link>
    <router-link to="/home">
      <button-list :isActive="listButtonState" @click.native="onClick(2)" />
    </router-link>
    <button-setting :isActive="settingButtonState" @click.native="onClick(3)" />
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
    homeButtonState: true,
    likeButtonState: false,
    listButtonState: false,
    settingButtonState: false
  }),
  methods: {
    changeState: function(index) {
      console.log(index)
      this.buttonState[this.activeNow] = false
      this.buttonState[index] = true
      this.activeNow = index
      console.log(this.activeNow, this.buttonState)
    },
    onClick: function(index) {
      this.homeButtonState = index === 0 ? true : false
      this.likeButtonState = index === 1 ? true : false
      this.listButtonState = index === 2 ? true : false
      this.settingButtonState = index === 3 ? true : false
    },
    routerPath() {
      // console.log('click')
      // console.log(this.$route)
      // this.$router.push('/home')
      // console.log(this.$route)
    }
  }
}
</script>

<style>
.sidebar-button {
  background-color: darkslategrey;
}
</style>
