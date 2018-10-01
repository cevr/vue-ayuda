<template>
  <div class="flex column search">
    <div class="flex header">
      <Icon icon="gear" />
      <Select :options="options" />
      <Button text="search" />
    </div>
    <div>criteria</div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

import Select from './Select.vue';
import Icon from './Icon.vue';
import Button from './Button.vue';

@Component({
  components: {
    Select,
    Icon,
    Button,
  },
})
export default class SearchCriteria extends Vue {
  private options = [{ key: 'Campaigns', value: 'campaigns' }];
}
</script>

<style scoped lang="less">
@import '../assets/less/variables.less';
.search {
  width: 300px;
  height: 100%;
  border-right: 1px #afd7ff solid;

  .header {
    background: @near-white;
    border-bottom: 1px solid #ccc;
    justify-content: space-around;
    padding: 10px 0;
  }

  .select {
    width: 55%;
    height: 30px;
    padding: 5px 10px;
  }
}
</style>