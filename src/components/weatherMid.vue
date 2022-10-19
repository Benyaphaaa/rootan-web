<template>
  <div
    class="d-flex flex-wrap flex-row gap-3 mt-2 justify-content-around box_middle"
  >
    <div class="box_mid rounded-4 d-flex justify-content-center">
      <div class="d-flex flex-column">
        <div class="d-flex justify-content-center mb-2">
          <div>12 : 00</div>
        </div>
        <img
          src="../assets/pic/rain.gif"
          width="110rem"
          height="auto"
          class="img-fluid rain-img"
          alt="rain"
        />
        <div class="d-flex justify-content-center">
          <div>26&deg;</div>
        </div>
      </div>
    </div>

    <div class="box_mid rounded-4 d-flex justify-content-center">
      <div class="d-flex flex-column">
        <div class="d-flex justify-content-center mb-1">
          <div>13 : 00</div>
        </div>
        <img
          src="../assets/pic/rain.gif"
          width="110rem"
          height="auto"
          class="img-fluid rain-img"
          alt="rain"
        />
        <div class="d-flex justify-content-center">
          <div>27&deg;</div>
        </div>
      </div>
    </div>

    <div class="box_mid rounded-4 d-flex justify-content-center">
      <div class="d-flex flex-column">
        <div class="edit_box_mid_1">
          <div>14 : 00</div>
        </div>
        <img
          src="../assets/pic/cloud.gif"
          width="120rem"
          height="auto"
          class="img-fluid cloud-img"
          alt="rain"
        />
        <div class="edit_box_mid_2 mt-1">
          <div>27&deg;</div>
        </div>
      </div>
    </div>

    <div class="box_mid rounded-4 d-flex justify-content-center">
      <div class="d-flex flex-column">
        <div class="edit_box_mid_1">
          <div>15 : 00</div>
        </div>
        <img
          src="../assets/pic/cloud.gif"
          width="120rem"
          height="auto"
          class="img-fluid cloud-img"
          alt="rain"
        />
        <div class="edit_box_mid_2 mt-1">
          <div>27&deg;</div>
        </div>
      </div>
    </div>

    <div class="box_mid rounded-4 d-flex justify-content-center">
      <div class="d-flex flex-column">
        <div class="edit_box_mid_1">
          <div>16 : 00</div>
        </div>
        <img
          src="../assets/pic/cloud.gif"
          width="120rem"
          height="auto"
          class="img-fluid cloud-img"
          alt="rain"
        />
        <div class="edit_box_mid_2 mt-1">
          <div>27&deg;</div>
        </div>
      </div>
    </div>

    <div class="box_mid rounded-4 d-flex justify-content-center">
      <div class="d-flex flex-column">
        <div class="edit_box_mid_1">
          <div>17 : 00</div>
        </div>
        <img
          src="../assets/pic/cloud.gif"
          width="120rem"
          height="auto"
          class="img-fluid cloud-img"
          alt="rain"
        />
        <div class="edit_box_mid_2 mt-1">
          <div>27&deg;</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@import "../assets/variables.scss";

.box_middle {
  div {
    font-size: 1.8rem;
    font-weight: 300;
  }
  .box_mid {
    padding: 1rem;
    width: 12rem;
    height: 15rem;
    background-color: $bg-inside;
  }
}
.edit_box_mid_1 {
  text-align: center;
  padding-bottom: 1.5rem;
}
.edit_box_mid_2 {
  text-align: center;
  padding-top: 2.5rem;
}

@media (min-width: 2560px) {
  .box_middle {
    width: 1836px;
    height: 345px;
    div {
      font-size: 37px;
    }
    .box_mid {
      width: 276.68px;
      height: 345.19px;
    }
  }

  .rain-img {
    width: 150px;
    padding-top: 15px;
    padding-bottom: 15px;
  }

  .cloud-img {
    width: 160px;
    padding-top: 25px;
    padding-bottom: 25px;
  }
}
</style>
