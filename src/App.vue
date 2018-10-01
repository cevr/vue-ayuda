<template>
  <div id="app">
    <div id="nav">
      <SideBar :routes="routes" />
    </div>
    <router-view />
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

import { SideBar } from './components';

@Component({
  components: { SideBar },
})
export default class App extends Vue {
  private routes = [{ path: '/', content: 'Home', icon: '' }, { path: '/about', content: 'About', icon: '' }];
}
</script>


<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
