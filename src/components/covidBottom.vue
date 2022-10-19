<template>
  <div class="box_end rounded-4">
    <div class="d-flex flex-column">
      <h2 class="header">
        โควิด - 19<img
          src="../assets/pic/logo_1.png"
          width="28rem"
          height="auto"
          class="img-fluid float-end mt-2 logo_1-img"
          alt="Ministry of Public Health"
        />
      </h2>
      <div class="d-flex justify-content-center">
        <img
          src="../assets/pic/covid.gif"
          width="140rem"
          height="auto"
          class="img-fluid covid-gif"
          alt="covid - 19"
        />
      </div>
      <div class="d-flex flex-row justify-content-around gap-5 setting-center">
        <div class="text-detail">รายใหม่</div>
        <div class="text-detail">เสียชีวิต</div>
      </div>
      <div class="d-flex flex-row justify-content-around gap-5">
        <div class="normal">23</div>
        <div class="normal">0</div>
      </div>
      <div class="d-flex flex-row justify-content-between mb-3 setting-center">
        <div class="text-detail">สะสม 86,519</div>
        <div class="text-detail">สะสม 1,037</div>
      </div>
      <div class="d-flex flex-row gap-1">
        <img
          src="../assets/pic/rootan-round.png"
          width="25rem"
          height="auto"
          class="img-fluid ph-img"
          alt="Ministry of Public Health"
        />
        <div class="text-small1">อัปเดตล่าสุด 24 ส.ค.</div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../assets/variables.scss";

.text-small1 {
  font-size: 1.05rem;
  font-weight: 300;
  color: $color-fade;
}

@media (min-width: 2560px) {
  .ph-img {
    width: 32px;
  }
  .text-small1 {
    font-size: 23px;
  }
}
</style>
