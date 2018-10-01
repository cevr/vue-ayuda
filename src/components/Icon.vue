<template>
  <span class="icon">
    {{icon}}
  </span>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class Icon extends Vue {
  @Prop({ required: true, default: '' })
  public icon!: string;
}
</script>

<style scoped lang="less">
@import '../assets/less/variables.less';

.icon {
  width: 24px;
  height: 24px;
  border: 1px solid @ayuda-orange;
  color: @ayuda-orange;
  background: #fff;
  border-radius: 6px;
  transition: ease-in-out 0.2s;
  cursor: pointer;

  &:hover {
    color: white;
    background: @ayuda-orange;
  }
}
</style>