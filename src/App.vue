<template>
  <div id="app">
    <h1>Vue eCharts Demo</h1>
    <div class="chart-wrapper">
      <chart :options="chartOptionsBar"></chart>
    </div>
    <div class="chart-wrapper">
      <chart :options="chartOptionsLine"></chart>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data: () => ({
      chartOptionsBar: {
        xAxis: {
          data: ['Q1', 'Q2', 'Q3', 'Q4']
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'bar',
            data: [63, 75, 25, 94]
          }
        ],
        title: {
          text: 'Quarterly Sales Results',
          x: 'center',
          textStyle: {
            fontSize: 24
          }
        },
        color: ['#128ac2']
      },

      chartOptionsLine: {
        xAxis: {
          data: [
            'Jan', 
            'Feb', 
            'Mar', 
            'Apr',
            'May',
            'Jun',
            'Jul',
            'Aug',
            'Sep',
            'Oct',
            'Nov',
            'Dec',
          ]
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'line',
            data: [63, 75, 25, 94, 76, 60, 90, 88, 71, 42, 59, 87]
          }
        ],
        title: {
          text: 'Monthly Stock Prices',
          x: 'center',
          textStyle: {
            fontSize: 24
          }
        },
        color: ['#128ac2']
      }
    })
  }
</script>

<style scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  
  .chart-wrapper{
    width: 100%;
    height: 700px;
  }

  .echarts{
    width:100%;
    height:100%;
  }
</style>
