<template>
  <d2-container>
    <template slot="header">限制显示条数环图</template>
    <div class="inner">
      <ve-ring :data="chartData" :settings="chartSettings" v-bind="pubSetting"></ve-ring>
    </div>
    <template slot="footer">
      <d2-link-btn title="更多示例和文档" link="https://v-charts.js.org"/>
    </template>
  </d2-container>
</template>

<script>
import list from '@/pages/demo/charts/list/_mixin/list.js'
export default {
  mixins: [
    list
  ],
  data () {
    this.chartSettings = {
      limitShowNum: 3
    }
    return {
      chartData: {
        columns: ['日期', '访问用户'],
        rows: [
          { '日期': '1/1', '访问用户': 1393 },
          { '日期': '1/2', '访问用户': 3530 },
          { '日期': '1/3', '访问用户': 2923 },
          { '日期': '1/4', '访问用户': 1723 },
          { '日期': '1/5', '访问用户': 3792 },
          { '日期': '1/6', '访问用户': 4593 }
        ]
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.inner {
  position: absolute;
  top: 20px;
  right:  20px;
  bottom: 20px;
  left: 20px;
}
</style>
