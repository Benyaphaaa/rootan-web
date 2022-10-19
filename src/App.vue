<template>
  <div>
    <img
      src="./assets/pic/live_icon1.png"
      class="live_img"
      style="font-size: 30px; cursor: pointer; position: absolute"
      @click="openNav"
    />
    <div class="container" v-if="infos.main">
      <div id="mySidenav" class="sidenav" style="text-align: center">
        <a href="javascript:void(0)" class="closebtn" @click="closeNav"
          >&times;</a
        >
        <img src="./assets/pic/live_in_box.png" alt="qwe" />
      </div>
      <div class="d-flex flex-wrap flex-row gap-4 mb-3 justify-content-center">
        <headerL :infos="infos.main" />
        <headerR />
      </div>
      <h2 class="text-weather">พยากรณ์อากาศ</h2>
      <weatherMid />
      <div
        class="d-flex flex-wrap flex-row gap-3 mt-4 justify-content-around box_last"
      >
        <covidBottom />
        <dengueBottom />
        <weatherBottom />
        <hotBottom :infos="infos.main" />
      </div>
    </div>
  </div>
  <div class="d-flex position-absolute end-0 bottom-0">
    <img src="./assets/pic/logo.png" class="img-fluid1" alt="LOGO" />
  </div>
</template>

<script setup>

import headerL from "./components/headerL.vue";
import headerR from "./components/headerR.vue";
import weatherMid from "./components/weatherMid.vue";
import hotBottom from "./components/hotBottom.vue";
import covidBottom from "./components/covidBottom.vue";
import dengueBottom from "./components/dengueBottom.vue";
import weatherBottom from "./components/weatherBottom.vue";
import { onMounted, ref } from "vue";

const infos = ref([]);

const lat = 14.0780167;
const lon = 100.606368;

onMounted(async () => {
  
  const response = await fetch(
    "https://api.openweathermap.org/data/2.5/weather?lat=" +
      
      lat +
      "&lon=" +
      lon +
      "&appid=3b82bd346aa885379ae8136478ba91d8"
  );
  
  const data = await response.json();
  
  infos.value = data;
  console.log(infos.value);
});

const openNav = () => {
  document.getElementById("mySidenav").style.width = "400px";
};
const closeNav = () => {
  document.getElementById("mySidenav").style.width = "0";
};


</script>

<style lang="scss">

@import "./assets/variables.scss";
.container {
  margin-top: 12px;
  .box_end {
    padding: 1.5rem;
    width: 19rem;
    height: 23rem;
    background-color: $bg-inside;
    .setting-center {
      align-items: center;
      .text-detail {
        font-size: 1.3rem;
        font-weight: 300;
      }
    }
  }
  .text-small {
    font-size: 1.05rem;
    font-weight: 300;
    color: rgba(241, 251, 255, 0.8);
  }
  .sidenav {
    height: 100%;
    width: 0;
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    background-color: $bg-inside;
    overflow-x: hidden;
    transition: 0.5s;
    padding-top: 60px;
    a {
      padding: 8px 8px 8px 32px;
      text-decoration: none;
      font-size: 25px;
      color: #818181;
      display: block;
      transition: 0.3s;
      &:hover {
        color: #f1f1f1;
      }
    }
    .closebtn {
      position: absolute;
      top: 0;
      right: 25px;
      font-size: 36px;
      margin-left: 50px;
    }
  }
  .normal {
    font-size: 2rem;
    font-weight: 500;
  }
}
.img-fluid1 {
  width: 18rem;
}

@media screen and (max-height: 450px) {
  .sidenav {
    padding-top: 15px;
    a {
      font-size: 18px;
    }
  }
}
@media (min-width: 2560px) {
  .header {
    font-size: 45px;
  }
  .logo_1-img {
    width: 40px;
  }
  .covid-gif {
    width: 190px;
  }

  .live_img {
    width: 150px;
  }
  .container {
    max-width: 1860px;
    margin-top: 50px;
    .normal {
      font-size: 45px;
    }
    .box_end {
      width: 426px;
      height: 494px;
      .setting-center {
        .text-detail {
          font-size: 30px;
        }
      }
      .img-end {
        padding-top: 10px;
        width: 32px;
      }
    }
    .text-small {
      padding-top: 10px;
      font-size: 23px;
    }
    .text-weather {
      margin-left: 7px;
      font-size: 45px;
      padding-top: 15px;
      padding-bottom: 15px;
    }
    .box_last {
      width: 1840px;
      height: 502px;
    }
  }
  .img-fluid1 {
    width: 330px;
  }
}
</style>
