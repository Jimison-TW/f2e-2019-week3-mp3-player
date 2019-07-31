<template>
  <div class="button-container">
    <icon :name="iconName" scale="100" style="fill: #05CE7C;"></icon>
    <p>{{ buttonText }}</p>
  </div>
</template>

<script>
export default {
  name: 'sidebar-button',
  props: {
    iconName: String,
    buttonText: String
  }
}
</script>

<style>
.svg-icon:active {
  fill: #ffffff
}

.button-container {
  height: 100px;
  color: #ffffff;
  background-color: gray
}
</style>
