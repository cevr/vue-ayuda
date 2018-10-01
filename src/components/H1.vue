<template>
  <span class="h1">{{text}}</span>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';
@Component
export default class H1 extends Vue {
  @Prop({ required: true, default: '' })
  public text!: string;
}
</script>

<style scoped lang="less">
.h1 {
  font-family: HelveticaNeue-Light, SegoeUI-Light-Large;
  -webkit-font-smoothing: antialiased;
  font-size: 20px;
}
</style>