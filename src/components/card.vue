<template>
  <div class="card">
    <div class="card__top">
      {{svgTop}}
      <h2>{{prName}}</h2>
    </div>
    <div class="bottom">
      <h2>{{prName}}</h2>
      <p>{{prSlogan}}</p>
      <p>{{prDes}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "card",
  props: ["svgTop", "prName", "prSlogn", "prDes"]
};
</script>

<style lang="scss" scoped>
.card {
  position: relative;
  width: calc(316px - 64px);
  height: calc(220px - 64px);
  background-color: #fff;
  box-shadow: 0 2px 4px 0 #ccd0d9;
  border-radius: 4px;
  margin-bottom: 16px;
  padding: 32px;
  cursor: pointer;
  transition: all 0.3s ease;

  &__top {
    position: relative;
    display: flex;
    justify-content: flex-start;
    align-items: center;

    svg {
      transition: all 0.3s ease;
    }

    &:after {
      content: "";
      display: block;
      position: absolute;
      right: 0;
      width: 24px;
      height: 24px;
      background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/945546/cards-arrow.svg")
        no-repeat;
      background-size: 16px;
      background-position: center;
      transform: translatex(-40%);
      transition: all 0.3s ease;
      opacity: 0;
    }

    h2 {
      font-weight: 400;
      margin-left: 12px;
      font-size: 18px;
      color: #ffffff;
      transform: translatex(-4%);
      transition: all 0.3s ease;
      opacity: 0;
    }
  }

  &__bottom {
    position: relative;
    margin-top: 24px;

    h2 {
      margin-top: 60px;
      margin-bottom: 8px;
      font-size: 18px;
      color: #292f3a;
      transition: all 0.3s ease;
    }
    p {
      transition: all 0.3s ease;
      &:nth-of-type(1) {
        opacity: 0.7;
        font-size: 14px;
        color: #292f3a;
        letter-spacing: 0;
        line-height: 21px;
      }
      &:nth-of-type(2) {
        opacity: 0;
        font-size: 13px;
        font-weight: 300;
        color: #C3D5FF;
        letter-spacing: 0;
        line-height: 19px;
        position: absolute;
        top: -40px;
        transform: translateY(10px);
      }
    }
  }

  &:hover {
    background-color: #3973ff;
    box-shadow: 0 6px 12px 0 rgba(41, 47, 58, 0.14);

    .card__top {
      &:after {
        opacity: 1;
        transform: translatex(0);
      }
      svg {
        #Combined-Shape {
          fill: #fff;
        }
        #Rectangle-13 {
          fill: url(#linearGradient-2) !important;
        }
      }

      h2 {
        opacity: 1;
        transform: translatex(0);
      }
    }

    .card__bottom {
      h2 {
        transform: translateY(-20px);
        opacity: 0;
      }
      p {
        &:nth-of-type(1) {
          transform: translateY(-20px);
          opacity: 0;
        }
        &:nth-of-type(2) {
          transform: translateY(0);
          opacity: 1;
        }
      }
    }

    span {
      opacity: 1;
      transform: scale(1);
    }
  }
  span {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: url("https://s3-us-west-2.amazonaws.com/s.cdpn.io/945546/bg-222.png")
      no-repeat;
    background-size: contain;
    background-position: left;
    opacity: 0;
    transition-delay: 0.3s;
    transform-origin: left;
    transform: scale(0.9);
    transition: all 0.4s ease;
  }
}
</style>
