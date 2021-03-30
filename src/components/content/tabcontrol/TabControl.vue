<!--  -->
<template>
  <div class="tab-control">
    <div
      v-for="(item, index) in titles"
      :key="index"
      :class="{ active: index === currentIndex }"
      @click="tabclick(index)"
    >
      <span>{{ item }}</span>
    </div>
  </div>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';

export default {
  //import引入的组件需要注入到对象中才能使用
  components: {},
  data() {
    //这里存放数据
    return {
      currentIndex: 0,
    };
  },
  props: {
    titles: {
      type: Array,
      default: [],
    },
  },
  //方法集合
  methods: {
    tabclick(index){
      this.currentIndex=index
      this.$emit('tabClick',index)
    }
  },
};
</script>
<style scoped>
.tab-control {
  display: flex;
  position: sticky;
  top: 44px;
  background: white;
  z-index: 9;
}
.tab-control div {
  text-align: center;
  flex: 1;
  height: 40px;
  line-height: 40px;
}
.active {
  color: pink;
}
.active span {
  padding-bottom: 5px;
  border-bottom: pink solid 2px;
}
</style>