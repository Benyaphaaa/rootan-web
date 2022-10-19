<template>
  <div class="box_end rounded-4">
    <div class="d-flex flex-column">
      <h2 class="header">
        ดัชนีความร้อน<img
          src="../assets/pic/logo_3.png"
          class="img-fluid float-end mt-2 logo_1-img"
          id="hot-img-mini"
          alt="Ellipse_yellow"
        />
      </h2>
      <div class="d-flex justify-content-center">
        <img
          src="../assets/pic/hot.gif"
          class="img-fluid"
          id="hot-gif"
          alt="heat"
        />
      </div>
      <div
        class="d-flex flex-row justify-content-between gap-5 mt-2 setting-center"
      >
        <div class="text-detail">ความรู้สึกเหมือน</div>
        <div class="normal">{{ feels_like }}&deg;C</div>
      </div>
      <div
        class="d-flex flex-row justify-content-between gap-5 mt-4 mb-2 setting-center"
      >
        <div class="text-detail">ความชื้นสัมพัทธ์</div>
        <div class="normal">{{ humidity }}%</div>
      </div>
      <div class="d-flex flex-row gap-1">
        <img
          src="../assets/pic/Ellipse_yellow.png"
          class="img-fluid img-end"
          alt="OPEN WEATHER"
          id="img-color"
        />
        <div class="text-small">ระวังเกิดตะคริวจากความร้อน</div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["infos"]);
const humidity = Math.round(props.infos.humidity);
const feels_like = Math.round(props.infos.feels_like - 273.15);
</script>

<style lang="scss">
#img-color {
  width: 25px;
}
#hot-img-mini {
  width: 32px;
}
#hot-gif {
  width: 130px;
}
@media (min-width: 2560px) {
  .hot-gif {
    width: 180px;
  }
  #img-color {
    width: 32px;
  }
  #hot-img-mini {
    width: 40px;
  }
  #hot-gif {
    width: 180px;
  }
}
</style>
