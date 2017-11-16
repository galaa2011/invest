<template>
  <div class="page-invests">
    <q-resize-observable @resize="onResize" />
    <q-card>
      <q-card-title>
        投资组合
      </q-card-title>
      <q-card-main>
        <chart style="height:50vh" :options="options1" ref="chart1" class="chart1"></chart>
      </q-card-main>
    </q-card>
    <q-card>
      <q-card-title>
        项目分布
      </q-card-title>
      <q-card-main>
      <chart style="height:40vh" :options="options2" ref="chart2" class="chart2"></chart>
      </q-card-main>
    </q-card>
  </div>
</template>
<script>
export default {
  data () {
    return {
      options1: {
        tooltip: {
          trigger: 'item',
          formatter: '{a} <br/>{b}: {c} ({d}%)'
        },
        legend: {
          data: ['飞飞象', '点胜网', '萌萌达', '卡布奇诺']
        },
        series: [
          {
            name: '投资项目',
            type: 'pie',
            selectedMode: 'single',
            radius: [0, '30%'],
            label: {
              normal: {
                position: 'inner'
              }
            },
            labelLine: {
              normal: {
                show: false
              }
            },
            data: [
              { value: 335, name: '飞飞象' },
              { value: 310, name: '点胜网' },
              { value: 234, name: '萌萌达' },
              { value: 135, name: '卡布奇诺' }
            ]
          },
          {
            name: '投资项目',
            type: 'pie',
            radius: ['40%', '55%'],
            label: {
              normal: {
                formatter: '{per|{d}%}',
                rich: {
                  per: {
                    color: '#eee',
                    backgroundColor: '#334455',
                    padding: [2, 4],
                    borderRadius: 2
                  }
                }
              }
            },
            data: [
              { value: 335, name: '飞飞象' },
              { value: 310, name: '点胜网' },
              { value: 234, name: '萌萌达' },
              { value: 135, name: '卡布奇诺' }
            ]
          }
        ]
      },
      options2: {
        color: ['#3398DB'],
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            type: 'shadow'
          }
        },
        legend: {
          data: ['zax']
        },
        grid: {
          top: '2%',
          left: '3%',
          right: '3%',
          bottom: '3%',
          containLabel: true
        },
        xAxis: [
          {
            name: '轮次',
            type: 'category',
            data: ['种子', '天使', 'A', 'B', 'C', 'D'],
            axisTick: {
              alignWithLabel: true
            }
          }
        ],
        yAxis: [
          {
            // name: '项目分布',
            type: 'value'
          }
        ],
        series: [
          {
            name: '投资个数',
            type: 'bar',
            barWidth: '60%',
            data: [1, 3, 5, 4, 2, 0]
          }
        ]
      }
    }
  },
  methods: {
    onResize (size) {
      this.$refs.chart1.resize()
      this.$refs.chart2.resize()
    }
  }
}
</script>
<style scoped>
.echarts {
  width: 100%;
}
</style>
