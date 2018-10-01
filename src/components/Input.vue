<template>
  <input :placeholder="placeholder" :type="type" :class="[...defaultClass, ...classList]"/>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class Input extends Vue {
  @Prop({ default: '' })
  public placeholder!: string;
  @Prop({ default: 'text' })
  public type!: string;
  @Prop()
  public onChange!: string;
  @Prop({ default: [] })
  public classList!: string[];

  private defaultClass = ['input'];
}
</script>

<style scoped lang='less'>
.input {
  font-size: 12px;
  color: #555;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out 0.15s, -webkit-box-shadow ease-in-out 0.15s;
  transition: border-color ease-in-out 0.15s, box-shadow ease-in-out 0.15s;
}
</style>