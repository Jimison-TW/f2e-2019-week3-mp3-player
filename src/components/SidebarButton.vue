<template>
  <button class="button-container">
    <slot></slot>
    <p>{{ buttonText }}</p>
  </button>
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
  fill: #ffffff;
}

.button-container {
  height: 100px;
  color: #ffffff;
  background-color: gray;
}
</style>
