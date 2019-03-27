<template>
  <div id="app">
    <card :prName="cardInfo.prName[0]"/>
    <card :prName="cardInfo.prName[1]"/>
  </div>
</template>

<script>
import card from "./components/card";

export default {
  name: "App",
  components: {
    card
  },
  data() {
    return {
      cardInfo: {
        prName: ["行为验证","深知"]
      }
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
