<template>
  <div class="box_end rounded-4">
    <div class="d-flex flex-column">
      <h2 class="header">
        สภาพอากาศ<img
          src="../assets/pic/logo_2.png"
          width="30rem"
          height="auto"
          class="img-fluid float-end mt-2 logo_1-img"
          alt="Ellipse_blue"
        />
      </h2>
      <div class="d-flex justify-content-center">
        <img
          src="../assets/pic/pm.gif"
          width="155rem"
          height="auto"
          class="img-fluid pm-gif"
          alt="PM 2.5"
        />
      </div>
      <div
        class="d-flex flex-row justify-content-between gap-5 mt-2 setting-center"
      >
        <div class="text-detail">PM 2.5</div>
        <div class="normal">26μg/m³</div>
      </div>
      <div
        class="d-flex flex-row justify-content-between gap-5 mt-4 mb-2 setting-center"
      >
        <div class="text-detail">เกณฑ์</div>
        <div class="normal">0 - 25</div>
      </div>
      <div class="d-flex flex-row gap-1">
        <img
          src="../assets/pic/Ellipse_blue.png"
          width="25rem"
          height="auto"
          class="img-fluid img-end"
          alt="CMU CCDC"
        />
        <div class="text-small">คุณภาพอากาศดีมาก</div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss">
@media (min-width: 2560px) {
  .pm-gif {
    width: 220px;
  }
}
</style>
