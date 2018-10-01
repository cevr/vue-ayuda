<template>
  <span class="h2">
    {{text}}
  </span>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class H2 extends Vue {
  @Prop({
    required: true,
    default: '',
  })
  public text!: string;
}
</script>

<style scoped lang="less">
.h2 {
  margin-top: 8px;
  font-size: 15px;
}
</style>