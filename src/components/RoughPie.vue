<template>
  <div id="pie"></div>
</template>

<script>
import { Pie } from "rough-viz";
import { putAttrsToObj } from "../mixins/putAttrsToObj";

export default {
  name: "RoughPie",
  mixins: [putAttrsToObj],
  mounted() {
    let pieAttr = this.putAttrsToObj;
    pieAttr.element = "#pie";

    pieAttr.fillWeight = 2;
    pieAttr.strokeWidth = 3;
    pieAttr.fillStyle = "cross-hatch";
    pieAttr.roughness = 4;

    const pie = new Pie(pieAttr);
    return pie;
  }
};
</script>
