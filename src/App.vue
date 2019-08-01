<template>
  <div id="app">
    <div id="outer-container">
      <div id="sidebar">
        <div class="sidebar-button">
          <IconHome />
          <p>首頁</p>
        </div>
      </div>
      <div id="content">
        <middle-page />
      </div>
    </div>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/> -->
  </div>
</template>

<script>
import MiddlePage from './views/MiddlePage'
import IconHome from '@/assets/icon/icon-home.svg'

export default {
  name: 'app',
  components: {
    MiddlePage,
    IconHome
  },
  data: () => ({
    btn_list: [
      { name: 'icon-home', text: '首頁' },
      { name: 'icon-home', text: '最愛' },
      { name: 'icon-home', text: '清單' },
      { name: 'icon-home', text: '設定' }
    ]
  })
}
</script>

<style>
html {
  height: 100%;
}

body {
  margin: 0;
  height: 100%;
  background-color: black;
}

#app {
  height: 100%;
}

#outer-container {
  display: table;
  width: 100%;
  height: 100%;
}

#sidebar {
  display: table-cell;
  width: 15%;
  height: 100%;
  vertical-align: top;
  background-color: #2d2d2d;
  text-align: center;
}

#content {
  display: table-cell;
  width: 85%;
  vertical-align: top;
}

.sidebar-button {
  background-color: darkslategrey;
}
</style>
