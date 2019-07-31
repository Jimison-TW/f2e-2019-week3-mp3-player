<template>
  <div class="button-container">
    <icon :name="iconName" scale="100" style="color:#010101"></icon>
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

<style scoped>
.button-container {
  width: 100px;
  height: 100px;
}
</style>
