<!--  -->
<template>
  <swiper>
    <swiper-item v-for="(item, index) in banners" :key="index">
      <a href="item.link">
        <img :src="item.image" alt=""  @load="imgLoad"/>
      </a>
    </swiper-item>
  </swiper>
</template>

<script>
//这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
//例如：import 《组件名称》 from '《组件路径》';

import { Swiper, SwiperItem } from "components/common/swiper";
export default {
  //import引入的组件需要注入到对象中才能使用
  components: {
    Swiper,
    SwiperItem
  },
  data:{
    isLoad:false
  },
  props:{//子组件使用props获取父组件传的数据，在父组件中使用bind传过来
    banners:{
      type:Array,
      default(){
        return []
      }
    }
  },
  //方法集合
  methods: {
    imgLoad(){
      if(!this.isLoad){
        this.$emit('swiperImgLoad')
        this.isLoad=true
      }
    }
  },
  created() {
    
  },
};
</script>
<style scoped>
</style>