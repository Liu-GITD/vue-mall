<!--  -->
<template>
  <div class="goods-list">
    <goods-list-item v-for="(item, index) in goods" :key="index" :goodsitem="item"></goods-list-item>
  </div>
</template>

<script>
import GoodsListItem from "./GoodsListItem";

export default {
  //import引入的组件需要注入到对象中才能使用
  components: {
    GoodsListItem,
  },
  data() {
    //这里存放数据
    return {};
  },
  props: {
    goods: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  //方法集合
  methods: {},
};
</script>
<style scoped>
.goods-list{
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>