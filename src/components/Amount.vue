<template>
  <span class="amount">
    {{amount}}
  </span>

</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class Amount extends Vue {
  @Prop({
    required: true,
    default: '0',
  })
  public amount!: string;
}
</script>

<style scoped lang="less">
.amount {
  float: left;
  margin: 8px 5px 0 5px;
  background: #aaa;
  color: #fff;
  font-weight: bold;
  font-size: 11px;
  border-radius: 9px;
  padding: 2px 6px;
  text-align: center;
  height: 15px;
  line-height: 15px;
}
</style>