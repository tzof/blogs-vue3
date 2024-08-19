<template>
  <div id="autoScale" :style="{ transform: `scale(${scale})` }">
    <div style="width: 1920px; height: 1080px" class="autoScaleBox">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import { debounce, min } from "lodash";
export default {
  name: "AutoScale",
  data() {
    return {
      scale: 1,
      windowInnerHeight: window.innerHeight,
      windowInnerWidth: window.innerWidtxwh,
    };
  },
  mounted() {
    this.resize();
    window.addEventListener("resize", this.resize);
  },
  destroyed() {
    window.removeEventListener("resize", this.resize);
  },
  methods: {
    resize() {
      return debounce(() => {
        this.scale = min([window.innerWidth / 1920, window.innerHeight / 1080]);
        (this.windowInnerHeight = window.innerHeight),
          (this.windowInnerWidth = window.innerWidth);
      }, 100)();
    },
  },
};
</script>
