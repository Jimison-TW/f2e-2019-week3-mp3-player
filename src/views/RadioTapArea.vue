<template>
  <div class="radio-container">
    <button-random :isActive="randomButtonState" @click.native="onClick(0)" />
    <button-previous :isActive="previousButtonState" @click.native="onClick(1)" />
    <button-play :isActive="playButtonState" @click.native="onClick(2)" />
    <button-next :isActive="nextButtonState" @click.native="onClick(3)" />
    <button-repeat :isActive="repeatButtonState" @click.native="onClick(4)" />
  </div>
</template>

<script>
import ButtonRandom from '../components/icon-button/ButtonRandom'
import ButtonPrevious from '../components/icon-button/ButtonPrevious'
import ButtonPlay from '../components/icon-button/ButtonPlay'
import ButtonNext from '../components/icon-button/ButtonNext'
import ButtonRepeat from '../components/icon-button/ButtonRepeat'

export default {
  name: 'radio-tap-area',
  components: {
    ButtonRandom,
    ButtonPrevious,
    ButtonPlay,
    ButtonNext,
    ButtonRepeat
  },
  data: () => ({
    randomButtonState: false,
    previousButtonState: false,
    playButtonState: false,
    nextButtonState: false,
    repeatButtonState: false
  }),
  methods: {
    onClick(index) {
      this.randomButtonState = index === 0 ? true : false
      this.previousButtonState = index === 1 ? true : false
      this.playButtonState = index === 2 ? true : false
      this.nextButtonState = index === 3 ? true : false
      this.repeatButtonState = index === 4 ? true : false
    }
  }
}
</script>

<style scoped>
.radio-container {
  width: 100%;
  height: 200px;
  background-color: cadetblue;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
