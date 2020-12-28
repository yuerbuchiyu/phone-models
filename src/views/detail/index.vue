<template>
  <van-swipe :loop="false" class="my-swipe" indicator-color="#102E43">
    <div class="a"></div>
    <van-swipe-item v-for="item of state[$route.query.models]" :key="item">
      <img :src="item" />
    </van-swipe-item>
  </van-swipe>
</template>

<script>
import { Swipe, SwipeItem } from "vant";
import { reactive } from "vue";
import huawei1 from "../../assets/imgs/huawei/huawei1.png";
import huawei2 from "../../assets/imgs/huawei/huawei2.png";
import huawei3 from "../../assets/imgs/huawei/huawei3.png";
import huawei4 from "../../assets/imgs/huawei/huawei4.png";
import xiaomi1 from "../../assets/imgs/xiaomi/xiaomi1.png";
import xiaomi2 from "../../assets/imgs/xiaomi/xiaomi2.png";
import xiaomi3 from "../../assets/imgs/xiaomi/xiaomi3.png";
import xiaomi4 from "../../assets/imgs/xiaomi/xiaomi4.png";
import oppo1 from "../../assets/imgs/oppo/oppo1.png";
import oppo2 from "../../assets/imgs/oppo/oppo2.png";
import oppo3 from "../../assets/imgs/oppo/oppo3.png";
import oppo4 from "../../assets/imgs/oppo/oppo4.png";
import vivo1 from "../../assets/imgs/vivo/vivo1.png";
import vivo2 from "../../assets/imgs/vivo/vivo2.png";
import vivo3 from "../../assets/imgs/vivo/vivo3.png";
import vivo4 from "../../assets/imgs/vivo/vivo4.png";
import smartisan1 from "../../assets/imgs/smartisan/smartisan1.png";
import smartisan2 from "../../assets/imgs/smartisan/smartisan2.png";
import smartisan3 from "../../assets/imgs/smartisan/smartisan3.png";
import smartisan4 from "../../assets/imgs/smartisan/smartisan4.png";
import smartisan5 from "../../assets/imgs/smartisan/smartisan5.png";
import smartisan6 from "../../assets/imgs/smartisan/smartisan6.png";
import meizu1 from "../../assets/imgs/meizu/meizu1.png";
import meizu2 from "../../assets/imgs/meizu/meizu2.png";
import meizu3 from "../../assets/imgs/meizu/meizu3.png";
import meizu4 from "../../assets/imgs/meizu/meizu4.png";

export default {
  name: "Detail",
  components: {
    VanSwipe: Swipe,
    VanSwipeItem: SwipeItem,
  },
  setup() {
    const state = reactive({
      phones: [
        {
          name: "华为",
          code: "huawei",
        },
        {
          name: "小米",
          code: "xiaomi",
        },
        {
          name: "OPPO",
          code: "oppo",
        },
        {
          name: "vivo",
          code: "vivo",
        },
        {
          name: "锤子",
          code: "smartisan",
        },
        {
          name: "魅族",
          code: "meizu",
        },
      ],
      huawei: [huawei1, huawei2, huawei3, huawei4],
      xiaomi: [xiaomi1, xiaomi2, xiaomi3, xiaomi4],
      oppo: [oppo1, oppo2, oppo3, oppo4],
      vivo: [vivo1, vivo2, vivo3, vivo4],
      meizu: [meizu1, meizu2, meizu3, meizu4],
      smartisan: [smartisan1, smartisan2, smartisan3, smartisan4, smartisan5, smartisan6],
    });
    return {
      state,
    };
  },
};
</script>

<style>
.van-swipe__indicator {
  width: 8px!important;
  height: 8px;
  background-color: #102E43;
}
.van-swipe__indicators {
  bottom: 66px;
}
</style>