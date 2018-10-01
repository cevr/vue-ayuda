<template>
  <div id="app">
    <SearchCriteria />
    <Search />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import { SearchCriteria, Search } from '../components';

@Component({
  components: {
    SearchCriteria,
    Search,
  },
})
export default class Home extends Vue {}
</script>

<style lang="less">
@import '../assets/less/variables.less';
@import '../assets/less/base.less';

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  height: 100%;
}
</style>
