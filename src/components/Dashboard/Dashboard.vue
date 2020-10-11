<template>
  <div>
    <div class="small">
      Line
      <line-chart :chart-data="datacollection"></line-chart>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Bar
      <bar-chart :chart-data="datacollection"></bar-chart>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Horizontal Bar
      <horizontal-bar :chart-data="datacollection"></horizontal-bar>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Doughnut
      <doughnut :chart-data="datacollection"></doughnut>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Pie
      <pie :chart-data="datacollection"></pie>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Polar Area
      <polar-area :chart-data="datacollection"></polar-area>
      <button @click="fillData()">Randomize</button>
    </div>
    <!---->
    <div class="small">
      Radar
      <radar :chart-data="datacollection"></radar>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Bubble
      <bubble :chart-data="datacollection"></bubble>
      <button @click="fillData()">Randomize</button>
    </div>
    <div class="small">
      Scatter
      <scatter :chart-data="datacollection"></scatter>
      <button @click="fillData()">Randomize</button>
    </div>
  </div>
</template>

<script>
import LineChart from "./componets/LineChart";
import BarChart from "./componets/BarChart";
import HorizontalBar from "./componets/HorizontalBar";
import Doughnut from "./componets/Doughnut";
import Pie from "./componets/Pie";
import PolarArea from "./componets/PolarArea";
import Radar from "./componets/Radar";
import Bubble from "./componets/Bubble";
import Scatter from "./componets/Scatter";

export default {
  components: {
    LineChart,
    BarChart,
    HorizontalBar,
    Doughnut,
    Pie,
    PolarArea,
    Radar,
    Bubble,
    Scatter,
  },
  data() {
    return {
      datacollection: {
        labels: [
          "En",
          "Feb",
          "Mar",
          "Abr",
          "May",
          "Jun",
          "Jul",
          "Ago",
          "Sep",
          "Oct",
          "Nov",
          "Dic",
        ],
        datasets: [
          {
            label: "Ventas",
            backgroundColor: "#f87979",
            data: [11, 42, 23, 34, 55, 66, 47, 18, 9, 10, 44, 12],
          },
          {
            label: "Compras",
            backgroundColor: "#3eaf7c",
            data: [31, 12, 53, 14, 95, 26, 46, 28, 79, 13, 34, 10],
          },
        ],
      },
    };
  },
  mounted() {
    //this.fillData();
  },
  methods: {
    fillData() {
      this.datacollection = {
        labels: [
          "En",
          "Feb",
          "Mar",
          "Abr",
          "May",
          "Jun",
          "Jul",
          "Ago",
          "Sep",
          "Oct",
          "Nov",
          "Dic",
        ],
        datasets: [
          {
            label: "Ventas",
            backgroundColor: "#f87979",
            data: [
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
            ],
          },
          {
            label: "Compras",
            backgroundColor: "#3eaf7c",
            data: [
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
              this.getRandomInt(),
            ],
          },
        ],
      };
    },
    getRandomInt() {
      return Math.floor(Math.random() * (50 - 5 + 1)) + 5;
    },
  },
};
</script>

<style>
.small {
  max-width: 600px;
  margin: 150px auto;
}
</style>
