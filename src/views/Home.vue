<template>
  <div class="flag">
    <div class="flag-center">
      <div class="flag-circle"></div>
    </div>
    <div class="flag-center">
      <div class="flag-teeth"></div>
    </div>
    <div class="flag-center" style="z-index: 4px">
      <div class="flag-katana">
        <img src="../assets/machete-silhouette.svg" alt="" />
      </div>
    </div>
    <div class="flag-center">
      <div class="flag-star"><div class="flag-star___suport"></div></div>
    </div>
    <div class="flag-poles">
      <div class="flag-poles__top"></div>
      <div class="flag-poles__bottom"></div>
    </div>
  </div>
</template>

<style lang="scss">
body {
  overflow: hidden;
}
* {
  margin: 0 auto;
  padding: 0;
}
.flag {
  height: 100vh;
  width: 100vw;
  &-center {
    height: 100vh;
    width: 100vw;
    position: absolute;
    z-index: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    @media only screen and (max-width: 700px) {
      transform: scale(0.68);
    }
  }
  &-circle {
    width: 19rem;
    height: 19rem;
    border: 1rem solid #efc704;
    border-radius: 100%;
    border-top-color: transparent;
    border-left-style: dashed;
    transform: rotate(-45deg);
    position: relative;
    &::after {
      border: 1.4rem solid #c10808;
      border-radius: 100%;
      width: 19rem;
      height: 19rem;
      content: "";
      display: block;
      border-top-color: transparent;
      margin: -20px;
      border-bottom-color: transparent;
      border-right-color: transparent;
      transform: rotate(90deg);
      position: absolute;
    }
    &::before {
      border: 1.2rem solid #070707;
      border-radius: 100%;
      width: 19rem;
      height: 19rem;
      content: "";
      display: block;
      border-top-color: transparent;
      margin: -18px;
      border-bottom-color: transparent;
      border-right-color: transparent;
      transform: rotate(67deg);
      position: absolute;
    }
  }
  &-star {
    transform: scale(0.5);
    margin-top: -166px;
    &___suport {
      width: 0;
      height: 0;
      position: relative;
      margin: 100px;
      display: block;
      border-right: 100px solid transparent;
      border-bottom: 70px solid #efc704;
      border-left: 100px solid transparent;
      transform: rotate(35deg);
      &::before {
        border-bottom: 80px solid #efc704;
        border-left: 30px solid transparent;
        border-right: 30px solid transparent;
        position: absolute;
        height: 0;
        width: 0;
        top: -45px;
        left: -65px;
        display: block;
        content: "";
        transform: rotate(-35deg);
      }
      &::after {
        position: absolute;
        display: block;
        top: 3px;
        left: -105px;
        width: 0px;
        height: 0px;
        border-right: 100px solid transparent;
        border-bottom: 70px solid #efc704;
        border-left: 100px solid transparent;
        transform: rotate(-70deg);
        content: "";
      }
    }
  }
  &-katana {
    width: 18rem;
    height: 18rem;
    position: relative;
    transform: translate(69px, 74px);
    img {
      width: 100%;
      height: 100%;
      filter: drop-shadow(0px 7px 0px #070707);
    }
  }
  &-teeth {
    width: 19rem;
    height: 19rem;
    border: 2rem dashed #efc704;
    border-radius: 100%;
    border-top-color: transparent;
    border-left-style: dashed;
    transform: rotate(-45deg);
    position: relative;
    &::after {
      border: 2.5rem solid #c10808;
      border-radius: 100%;
      width: 19rem;
      height: 19rem;
      content: "";
      display: block;
      border-top-color: transparent;
      margin: -37px;
      border-bottom-color: transparent;
      border-right-color: transparent;
      transform: rotate(90deg);
      position: absolute;
    }
    &::before {
      border: 2.3rem solid #070707;
      border-radius: 100%;
      width: 19rem;
      height: 19rem;
      content: "";
      display: block;
      border-top-color: transparent;
      margin: -35px;
      border-bottom-color: transparent;
      border-right-color: transparent;
      transform: rotate(67deg);
      position: absolute;
    }
  }
  &-poles {
    &__bottom {
      height: 50vh;
      background: #070707;
      width: 100vw;
    }
    &__top {
      height: 50vh;
      background: #c10808;
      width: 100vw;
    }
  }
}
</style>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Katana from "@/components/Katana.vue"; // @ is an alias to /src

@Options({
  components: {
    Katana,
  },
})
export default class Home extends Vue {}
</script>
