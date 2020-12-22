<template>
  <van-cell-group>
    <van-cell
      v-for="phone of state.phones"
      :key="phone.code"
      is-link
      @click="showPopup"
      >{{ phone.name }}</van-cell
    >
  </van-cell-group>
  <van-popup
    position="bottom"
    round
    :style="{ height: '90%' }"
    v-model:show="show"
  >
    <div class="bar"></div>
  </van-popup>
</template>

<script>
import { Cell, Popup, CellGroup } from "vant";
import { reactive, ref } from "vue";

export default {
  name: "Home",
  components: {
    VanCell: Cell,
    VanPopup: Popup,
    VanCellGroup: CellGroup,
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
    });
    const show = ref(false);
    const showPopup = () => {
      show.value = true;
    };
    return {
      show,
      showPopup,
      state,
    };
  },
};
</script>

<style scoped>
.bar {
  height: 6px;
  width: 50px;
  background-color: #ccc;
  border-radius: 16px;
  margin: 5px auto;
}
</style>