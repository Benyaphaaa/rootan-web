<template>
  <div class="box_end rounded-4">
    <div class="d-flex flex-column">
      <h2 class="header">
        ไข้เลือดออก<img
          src="../assets/pic/logo_1.png"
          width="28rem"
          height="auto"
          class="img-fluid float-end mt-2 logo_1-img"
          alt="Dengue"
        />
      </h2>
      <div class="d-flex justify-content-center">
        <img
          src="../assets/pic/mosquito.gif"
          width="130rem"
          height="auto"
          class="img-fluid mosquito-gif"
          alt="covid - 19"
        />
      </div>
      <div class="d-flex flex-row justify-content-between gap-5 setting-center">
        <div class="text-detail">จำนวนผู้ป่วย</div>
        <div class="normal">4</div>
        <div class="text-detail">คน</div>
      </div>
      <div
        class="d-flex flex-row justify-content-between gap-5 mt-4 mb-2 setting-center"
      >
        <div class="text-detail">ค่าเฉลี่ย</div>
        <div class="normal zero">0</div>
        <div class="text-detail">คน</div>
      </div>
      <div class="d-flex flex-row gap-1">
        <img
          src="../assets/pic/Ellipse_green.png"
          width="25rem"
          height="auto"
          class="img-fluid img-end"
          alt="Ministry of Public Health"
        />
        <div class="text-small">เสี่ยงต่อการเป็นโรคไข้เลือดออกต่ำ</div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../assets/variables.scss";

.zero {
  margin-left: 40px;
}
@media (min-width: 2560px) {
  .mosquito-gif {
    width: 180px;
  }
}
</style>
