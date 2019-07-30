<template>
  <div class="btn-container">
    <slot></slot>
    <p>{{ iconName }}</p>
  </div>
</template>

<script>
export default {
  name: 'SideBarButton',
  props: {
    iconName: String
  }
}
</script>

<style>
.btn-container{
  width: 100;
}
</style>
