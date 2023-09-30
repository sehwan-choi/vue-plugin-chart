<template>
    <canvas ref="lineChart" id="lineChart"></canvas>
</template>

<script>
export default {
    props: ['line'],
    mounted() {
        console.log(this.line);
        var ctx = this.$refs.lineChart.getContext('2d');
        new this.$_Chart(ctx, {
            // The type of chart we want to create
            type: 'line',

            // The data for our dataset
            data: {
                labels: ["January", "February", "March", "April", "May", "June", "July"],
                datasets: this.line
            },

            // Configuration options go here
            options: {}
        });
    }
}
</script>

<style>

</style>