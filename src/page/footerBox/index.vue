<script setup lang="ts">
const onClickICP = () => {
  window.open("https://beian.miit.gov.cn");
};
</script>

<template>
  <div class="footer">
    <span class="icp" @click="onClickICP">浙ICP备2024102715号-1</span>
  </div>
</template>

<style scoped lang="less">
.footer {
  width: 100%;
  display: flex;
  justify-content: center;
  position: fixed;
  bottom: 0;
  background-color: #ececec;
  .icp {
    cursor: pointer;
    &:hover {
      text-decoration: underline;
      color: #315efb;
    }
  }
}
</style>
