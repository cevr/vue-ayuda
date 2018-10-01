<template>
  <button class="btn btn-primary btn-sm">
    {{text}}
  </button>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class Button extends Vue {
  @Prop({ default: '' })
  public text!: string;

  @Prop({ default: 'primary' })
  public type!: string;

  @Prop({ default: 'small' })
  public size!: string;
}
</script>

<style scoped lang="less">
@import '../assets/less/variables.less';

button {
  cursor: pointer;
  transition: ease-in-out 0.2s;
  &:hover {
    background: lighten(@ayuda-orange, 20%);
    border-color: lighten(@btn-border, 20%);
  }
}

.btn {
  height: 30px;
}
.btn-primary {
  background-color: @ayuda-orange;
  border-color: @btn-border;
  color: #fff;
}

.btn-sm {
  font-size: 12px;
  line-height: 1.5;
  border-radius: 3px;
}
</style>