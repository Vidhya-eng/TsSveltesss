<script lang="ts">
	 import {onMount} from "svelte";
     import * as echarts from "echarts";
function createChart(){
   
// initialize the echarts instance


let chart = echarts.init(<HTMLDivElement>document.getElementById("main"), {});
// Draw the chart
chart.setOption({
    title: {
        text: 'ECharts Getting Started Example'
    },
    tooltip: {},
    xAxis: {
        data: ['shirt', 'cardigan', 'chiffon', 'pants', 'heels', 'socks']
    },
    yAxis: {},
    series: [{
        name: 'sales',
        type: 'bar',
        data: [5, 20, 36, 10, 10, 20]
    }]
});
}
onMount(createChart);
</script>

<body>
    <!-- preparing a DOM with width and height for ECharts -->
    <div id="main" style="width:600px; height:400px;"></div>
</body>
