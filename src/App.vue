<template>
  <div>
    <h1>Chart.js</h1>
    <bar-chart></bar-chart>
    <line-chart :line="lineData"></line-chart>
  </div>
</template>

<script>
import BarChart from './components/BarChart.vue'
import LineChart from './components/LineChart.vue'

export default {
  components: { BarChart, LineChart },
  data() {
    return {
      lineData: [{
        label: "My First dataset",
        backgroundColor: 'rgb(255, 99, 132)',
        borderColor: 'rgb(255, 99, 132)',
        data: [0, 10, 5, 2, 20, 30, 45],
      }],
    }
  }
}
</script>

<style>

</style>