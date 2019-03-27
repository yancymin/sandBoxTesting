<template>
  <div id="app">
    <card
      :svgTop="cardInfo.svgTop()"
      :prName="cardInfo.prName[0]"
      :prSlogan="cardInfo.prSlogan[0]"
      :prDes="cardInfo.prDes[0]"
    />
    <card :prName="cardInfo.prName[1]"/>
    <card :prName="cardInfo.prName[1]"/>
  </div>
</template>

<script>
import card from "./components/card";
import deepknow from "./assets/deepknow.svg";

export default {
  name: "App",
  components: {
    card,
    deepknow
  },
  data() {
    let svgLogo =
    return {
      cardInfo: {
        svgTop: function() {
          let svgLogo = document.getElemntr
          // return deepk
        },
        prName: ["行为验证", "深知"],
        prSlogan: ["人机验证 3.0 通用型解决方案(基于生物行为与人工智能)", ""],
        prDes: [
          " 使用 AI 动态判断网站当前的攻击势态，并结合每次请求的多维度数据组合，AI 能够做到对每一次请求使用不同的防御能力组合，采用不同的决策方案，确保做到网站安全和体验的最优均衡。"
        ]
      }
    };
  }
};
</script>

<style>
body {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  background-color: #f1f5fb;
}
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 980px;
  padding: 40px 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-content: flex-start;
}
</style>
