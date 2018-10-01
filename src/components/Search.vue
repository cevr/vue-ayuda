<template>
  <div class="flex column table">
    <div class="flex header">
      <div class="flex">
        <Icon icon="f" />
        <H1 text="Campaign" />
        <Amount amount="36,984" />
        <Icon icon="+" />
        <Icon icon="u" />
        <Icon icon="o" />
        <H2 text="Selected" />
        <Amount />
        <Input placeholder="Search campaigns" type="text" :classList="['search']"/>
        <Icon icon="s" />
      </div>
      <div class="flex">
        <span>Show</span>
        <Select :options="options" />
        <span>
          1 2 3 4 5
        </span>
      </div>
    </div>
    <div class="flex">
      table
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

import Icon from './Icon.vue';
import H1 from './H1.vue';
import H2 from './H2.vue';
import Amount from './Amount.vue';
import Select from './Select.vue';
import Input from './Input.vue';

@Component({
  components: { Icon, H1, H2, Amount, Select, Input },
})
export default class Search extends Vue {
  private options = [
    {
      key: '25',
      value: 25,
    },
  ];
}
</script>

<style scoped lang="less">
@import '../assets/less/variables.less';

.table {
  height: 100%;
  width: 100%;

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: @header-color;
    background: @header-bg;
    height: 58px;
    margin: 1px;
    width: 100%;

    span {
      margin: 5px;
    }

    .search {
      height: 20px;
      width: 160px;
      padding-left: 18px;
      margin-top: 5px;
      &::placeholder {
        font-style: italic;
      }
    }
  }
}
</style>