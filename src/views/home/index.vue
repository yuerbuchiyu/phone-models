<template>
  <van-cell-group>
    <router-link v-for="phone of state.phones" :key="phone.code" :to="{path: 'detail', query:{models: phone.code }}">
      <van-cell is-link>
        {{ phone.name }}
      </van-cell>
    </router-link>
  </van-cell-group>
</template>

<script>
import { Cell, CellGroup } from "vant";
import { reactive } from "vue";

export default {
  name: "Home",
  components: {
    VanCell: Cell,
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
    return {
      state
    };
  },
};
</script>

<style scoped>
</style>