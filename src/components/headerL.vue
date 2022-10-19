<template>
  <div class="box_left rounded-4">
    <div class="d-flex flex-column">
      <div class="d-flex flex-row gap-2"></div>
      <div class="normal">
        <img
          src="@/assets/pic/location.png"
          width="40rem"
          height="auto"
          alt="location"
          class="location-img"
        />
        คลองหนึ่ง
        <img
          src="@/assets/pic/rootan-logo1.png"
          width="100rem"
          height="auto"
          class="logo-img"
          alt="location"
        />
      </div>
      <div class="font-thin" id="pad">คลองหนึ่ง ปทุมธานี</div>
      <div class="d-flex flex-row gap-3">
        <div>
          <img
            src="@/assets/pic/cloud-sun.gif"
            class="sun-img"
            alt="sun_could"
          />
        </div>
        <div class="main-temp">{{ temp }}&deg;</div>
        <div
          class="d-flex flex-row justify-content-center align-items-end"
          id="m-fix"
        >
          <div class="d-flex flex-column">
            <!-- เอาตัวแปรไปใช้โดยการใส่ {{ตัวแปร}} -->
            <div class="font-thin">{{ temp_min }}&deg;</div>
            <div class="font-thin">{{ temp_max }}&deg;</div>
          </div>
          <div class="d-flex flex-column">
            <div class="bold">เมฆเล็กน้อย</div>
            <div class="last-date">ล่าสุด 25 ส.ค. 11.38</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// ? ค่าที่ส่งมาจะเรียกด้วยการประกาศ defineProps(['ค่าที่ส่งมา  1','ค่าที่ส่งมา 2'])
const props = defineProps(["infos"]);
// ? เอาค่าที่ส่งมาไปดึงค่าที่ต้องการและเก็บลงตัวแปร
const temp = Math.round(props.infos.temp - 273.15);
const temp_min = Math.round(props.infos.temp_min - 273.15);
const temp_max = Math.round(props.infos.temp_max - 273.15);
console.log(props.infos);
</script>

<style lang="scss">
@import "../assets/variables.scss";
.sun-img {
  width: 180px;
}

.box_left {
  padding: 1rem 1.5rem 1.5rem 1.5rem;
  width: 46rem;
  height: 15rem;
  background-color: $bg-inside;

  .logo-img {
    margin-left: 400px;
  }

  .font-thin {
    font-size: 1.5rem;
    font-weight: 300;
  }
  .main-temp {
    font-size: 6rem;
  }
  #m-fix {
    margin-bottom: 2rem;
    .last-date {
      letter-spacing: 2px;
      padding-left: 2.5rem;
      font-size: 1.6rem;
      font-weight: 300;
      color: $color-fade;
    }
    .bold {
      padding-left: 2.5rem;
      font-size: 2rem;
      font-weight: 500;
      color: $color-fade;
    }
  }
}

@media (min-width: 2560px) {
  .box_left {
    width: 1011.85px;
    height: 416.3px;
    .logo-img {
      width: 140px;
      margin-left: 520px;
    }
    .location-img {
      width: 70px;
      padding-left: 10px;
    }
    #pad {
      padding-top: 10px;
      padding-left: 10px;
    }
    .font-thin {
      font-size: 37px;
    }
    .sun-img {
      width: 300px;
      padding-top: 10px;
    }
    .main-temp {
      font-size: 148px;
      padding-top: 30px;
    }
    #m-fix {
      .last-date {
        font-size: 37px;
      }
      .bold {
        font-size: 45px;
      }
    }
  }
}
</style>
