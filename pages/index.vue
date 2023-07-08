<template>
  <n-layout>
    <n-layout-header>
      <n-image
          class="headerImg"
          src="https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg"
      />
      <n-button v-for="item in btnList"  class="ml-14" text>{{item.text}}</n-button>
    </n-layout-header>
    <n-layout-content content-style="padding: 5px;">
      <n-carousel class="rounded-1xl" show-arrow autoplay>
        <img v-for="imgUrl in imgList"
            class="carousel-img"
            :src="imgUrl"
        >
      </n-carousel>

    </n-layout-content>
    <n-layout-footer >
      <n-card title="职场技能 助你提高职场竞争力">
        <n-grid x-gap="12" :cols="4" y-gap="12">
          <n-gi  v-for="i in Lessonlist">
            <n-card title="计算机培训内容" class="card-item"  hoverable >
              <template #cover>
                <img src="https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg">
              </template>
              免费
            </n-card>
          </n-gi>
        </n-grid>
      </n-card>
      <n-card title="互联网技术 每一门都是好课程" class="my-8" >
        <n-grid x-gap="12" :cols="4" y-gap="12">
          <n-gi  v-for="i in Lessonlist">
            <n-card title="计算机培训内容" class="card-item" hoverable>
              <template #cover>
                <img src="https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel1.jpeg">
              </template>
              免费
            </n-card>
          </n-gi>
        </n-grid>
      </n-card>
      <n-card title="工业制造 再造业培训" >
        <n-grid x-gap="12" :cols="4" y-gap="12">
          <n-gi  v-for="i in Lessonlist">
            <n-card title="计算机培训内容" class="card-item" hoverable>
              <template #cover>
                <img src="https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg">
              </template>
              免费
            </n-card>
          </n-gi>
        </n-grid>
      </n-card>
    </n-layout-footer>
  </n-layout>

</template>

<script setup>
import {NButton,NLayout,NLayoutHeader,NLayoutFooter,NLayoutContent,NCarousel,NImage,NCard,NGrid,NGi} from "naive-ui"
let a = "测试一下"
let btnList = [
  {
    "text":"课程中心",
    "type":"text"
  },
  {
    "text":"课程中心",
    "type":"text"
  },
  {
    "text":"课程中心",
    "type":"text"
  },
  {
    "text":"课程中心",
    "type":"text"
  },
]
let Lessonlist = [1,2,3,4,5]
let imgList = [
    "https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg",
    "https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg",
    "https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel2.jpeg"
]
let b = ()=>{
  console.log("测试")
}
</script>

<style scoped>
.n-layout{
 display: flex;
  flex-direction: column;
  --tw-bg-opacity: 1;
  background: rgba(249, 250, 251, var(--tw-bg-opacity));
  align-items: center;

}

.n-layout-header{
  height: 70px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

}

.headerImg{
  width: 100px;
  height: 50px;
}

.n-layout-content {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.n-carousel{
  width: 1200px;
  height: 400px;
}
.carousel-img {
  width:1200px;
  height: 400px;
  object-fit: cover;
}

.n-layout-footer{
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  width:1200px;
  height: auto;
}

.card-item{
  max-width: 300px;
  height:200px;
}

</style>