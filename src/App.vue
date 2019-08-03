<template>
  <div id="app">
    <div id="outer-container">
      <div id="sidebar">
        <sidebar-area />
      </div>
      <div id="content">
        <!-- <middle-page /> -->
         <router-view/>
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
import SidebarArea from './components/SidebarArea'

export default {
  name: 'app',
  components: {
    MiddlePage,
    SidebarArea
  },
  data: () => ({
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
</style>
