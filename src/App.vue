<template>
  <div id="app">
    <div id="outer-container">
      <div id="sidebar">
        <IconHome />
        <!-- <SideBarButton :iconName="iconNameList[0]">
          <IconHome />
        </SideBarButton> -->
      </div>
      <div id="content"></div>
    </div>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/> -->
  </div>
</template>

<script>
// import SideBarButton from '@/components/SideBarButton'
// import IconHome from '@/assets/icon/icon-home.svg'
import IconHome from '@/components/icon_button/IconHome'

export default {
  name: 'app',
  components: {
    // SideBarButton,
    IconHome
  },
  data: () => ({
    iconNameList: '首頁'
  })
}
</script>

<style>
#app,
html {
  background-color: black;
  height: 100%;
}

#app,
body {
  margin: 0;
  height: 100%;
}

#outer-container {
  display: table;
  width: 100%;
  height: 100%;
}

#sidebar {
  display: table-cell;
  width: 20%;
  vertical-align: top;
  background-color: brown;
}

#content {
  display: table-cell;
  width: 85%;
  vertical-align: top;
}
</style>
