<!--  -->
<template>
  <div class="nav-bar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
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
    return {};
  },
  //方法集合
  methods: {},
};
</script>
<style scoped>

  .nav-bar{
    display: flex;
    height: 44px;
    line-height: 44px;
    text-align: center;
    color: white;
    background: rgba(250, 166, 166);
    box-shadow: 0 1px 1px rgba(250, 166, 166, 0.479);
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 9;
  }
  .left,.right{
    width: 60px;
    /* background: chartreuse; */
  }
  .center{
    flex: 1;
    /* background: red; */
  }
</style>