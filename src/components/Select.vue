<template>
  <select
    name="name"
    class="input select"
  >
    <option
      v-for="option of options"
      :value="option.value"
      :key="option.value"
    >{{option.key}}</option>
  </select>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

interface Select {
  key: string;
  value: string;
}
@Component
export default class SelectComponent extends Vue {
  @Prop({ default: [] })
  public options!: Select[];
}
</script>

<style scoped lang="less">
.select {
  height: 20px;
  width: 58px;
  margin-top: 5px;
}
</style>