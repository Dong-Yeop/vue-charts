<template>
  <canvas ref="barChart"></canvas>
</template>

<script>
export default {
  props: ['propsdata'],
  mounted() {
    const ctx = this.$refs.barChart;
    const myChart = new this.$_Chart(ctx, {
        type: 'bar',
        data: {
            labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
            datasets: this.propsdata
        },
        options: {
            scales: {
                y: {
                    beginAtZero: true
                }
            }
        }
    });
    console.log(myChart);
  }
}
</script>

<style>

</style>