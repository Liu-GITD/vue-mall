<!--  -->
<template>
  <div class="recommend">
    <div v-for="(item,index) in recommends" :key="index" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
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
    return {};
  },
  props:{
    recommends:{
      type:Array,
      default:[]
    }
  },
  //方法集合
  methods: {},
};
</script>
<style scoped>


.recommend{
  display: flex;
  text-align: center;
  font-size: 12px;
  padding: 15px 0 30px;
  border-bottom: 8px solid #eee;
}

.recommend-item{
  flex:1;
}
.recommend-item div{
  padding-top: 2px;
}
img{
  width: 80px;
  height: 80px;
}
</style>