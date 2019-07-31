<template>
  <div id="app">
    <div id="outer-container">
      <div id="sidebar">
        <div v-for="(item, index) in btn_list" :key="index">
          <sidebar-button :iconName="item.name" :buttonText="item.text" />
        </div>
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
import SidebarButton from '@/components/SidebarButton'

export default {
  name: 'app',
  components: {
    SidebarButton
  },
  data: () => ({
    btn_list: [
      { name: 'icon-home', text: '首頁' },
      { name: 'icon-home', text: '首頁' },
      { name: 'icon-home', text: '首頁' }
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
  background-color: brown;
}

#content {
  display: table-cell;
  width: 85%;
  vertical-align: top;
}
</style>
