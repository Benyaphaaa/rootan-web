<template>
  <div class="box_right rounded-4 box_top_right">
    <div
      id="carouselExampleControls"
      class="carousel slide"
      data-bs-ride="carousel"
    >
      <div class="carousel-inner">
        <div class="carousel-item active">
          <a
            href="https://www.facebook.com/myRooTan/photos/a.107497541570626/392017786451932/"
          >
            <img
              src="../assets/pic/banner1.png"
              class="w-100 img-fluid2"
              alt="banner1"
            />
            <img
              src="../assets/pic/banner1-large.png"
              class="img-fluid2-large"
              alt="banner1"
            />
          </a>
        </div>
        <div class="carousel-item">
          <a
            href="https://www.facebook.com/photo/?fbid=393632039475521&set=pcb.393632446142147"
          >
            <img
              src="../assets/pic/banner2.png"
              class="w-100 img-fluid2"
              alt="banner1"
            />
            <img
              src="../assets/pic/banner2-large.png"
              class="img-fluid2-large"
              alt="banner1"
            />
          </a>
        </div>
        <div class="carousel-item">
          <a
            href="https://www.facebook.com/photo/?fbid=362514016027595&set=a.249595700652761"
          >
            <img
              src="../assets/pic/banner3.png"
              class="w-100 img-fluid2"
              alt="banner1"
            />
            <img
              src="../assets/pic/banner3-large.png"
              class="img-fluid2-large"
              alt="banner1"
            />
          </a>
        </div>
        <div class="carousel-item">
          <a
            href="https://www.facebook.com/photo/?fbid=390639603096869&set=a.309744487853048"
          >
            <img
              src="../assets/pic/banner4.png"
              class="w-100 img-fluid2"
              alt="banner1"
            />
            <img
              src="../assets/pic/banner4-large.png"
              class="img-fluid2-large"
              alt="banner1"
            />
          </a>
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExampleControls"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExampleControls"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.box_right {
  width: 33rem;
  height: 15rem;
  .img-fluid2-large {
    display: none;
  }
}

@media (min-width: 2560px) {
  .box_top_right {
    width: 800px;
    .img-fluid2 {
      display: none;
      width: 517.36px;
      height: 293px;
    }
    .img-fluid2-large {
      margin-left: 10px;
      display: block;
      width: 780px;
      height: 416.3px;
    }
  }
}
</style>
