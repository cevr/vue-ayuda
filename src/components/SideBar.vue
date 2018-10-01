<template>
  <div class="sidebar">
    <div
      class="item"
      v-for="route in routes"
      v-on:click="routeTo(route.path)"
      :key="route.path"
      :class="{active: $route.path === route.path}"
    >
      {{route.icon}}
      {{route.content}}
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

interface Route {
  path: string;
  content: string;
  icon: string;
}

@Component
export default class SideBarComponent extends Vue {
  @Prop({ required: true, default: [] })
  public routes!: Route[];

  private routeTo(path: string): void {
    this.$router.push(path);
  }
}
</script>

<style scoped lang="less">
.sidebar {
  display: flex;
  flex-direction: column;
  background: #7c94a6;
  box-shadow: inset -1px 1px 12px rgba(0, 0, 0, 0.2);

  .item {
    height: 60px;
    width: 100px;
    color: white;
    transition: ease 0.25s;
    &.active {
      background: white;
      color: #5b5e63;
      box-shadow: -5px 1px 8px rgba(0, 0, 0, 0.2);
    }
  }
}
</style>