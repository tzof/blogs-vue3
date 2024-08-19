<script setup lang="ts">
import footerBox from "@/page/footerBox/index.vue";
import AutoScale from "@/components/AutoScale.vue";
</script>

<template>
  <div class="app">
    <AutoScale>
      <router-view />
      <footerBox />
    </AutoScale>
  </div>
</template>

<style scoped lang="less">
.app {
  position: relative;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  //   background-image: url("@/images/header/bg.png");
  //   background-size: 100% 100%;
  //   background-repeat: no-repeat;
  //   background-position: center center;
  /deep/.autoScaleBox {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: #fff;
  }
}
</style>
