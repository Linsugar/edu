<template>
  <n-layout>
    <n-layout-header>颐和园路</n-layout-header>
    <n-layout-content content-style="padding: 5px;">
      <n-carousel class="rounded-1xl">
        <img
            class="carousel-img"
            src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel1.jpeg"
        >
        <img
            class="carousel-img"
            src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg"
        >
        <img
            class="carousel-img"
            src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel3.jpeg"
        >
        <img
            class="carousel-img"
            src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel4.jpeg"
        >
      </n-carousel>
    </n-layout-content>
    <n-layout-footer>成府路</n-layout-footer>
  </n-layout>

</template>

<script setup>
import {NButton,NLayout,NLayoutHeader,NLayoutFooter,NLayoutContent,NCarousel} from "naive-ui"
let a = "测试一下"
let b = ()=>{
  console.log("测试")
}
</script>

<style scoped>
.n-layout{
 display: flex;
  flex-direction: column;


}

.n-layout-header,
.n-layout-footer {
  background: rgba(128, 128, 128, 0.2);
  padding: 24px;
  display: flex;
  flex-direction: row;

}

.n-layout-sider {
  background: rgba(128, 128, 128, 0.3);
}

.n-layout-content {
  background: rgba(128, 128, 128, 0.4);
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.n-carousel{
  width: 900px;
  height: 400px;
}
.carousel-img {
  width: 900px;
  height: 400px;
  object-fit: cover;
}
</style>