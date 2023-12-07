<script setup>
import { RouterLink, RouterView } from "vue-router";
import Header from "./components/Header.vue";


</script>
<script>
export default{
    data(){
        return{
            loader:"loader",
            stop:"stop",
            page:false
        }
    },
    mounted(){
        setTimeout(()=>{
            this.loader=this.stop
        },5000)
      
    },
    methods:{
      getChPage(xxx){
        this.page=xxx
        // console.log(this.page);
      }
    }
}
</script>

<template>
  <div class="header">
    <Header @pageCh="getChPage" />
  </div>
  <div class="del"></div>
  <div class="content" v-if="page==false">
    <div :class="loader">
    <div class="box">
        <div class="square" ></div>
        <div class="square"></div>
        <div class="square last"></div>
        <div class="square clear"></div>
        <div class="square"></div>
        <div class="square last"></div>
        <div class="square clear"></div>
        <div class="square "></div>
        <div class="square last"></div>
    </div>
</div>
<div class="contentBox">
  <RouterView />
</div>
  </div>
  <div class="content1" v-else>
    <div :class="loader">
    <div class="box">
        <div class="square" ></div>
        <div class="square"></div>
        <div class="square last"></div>
        <div class="square clear"></div>
        <div class="square"></div>
        <div class="square last"></div>
        <div class="square clear"></div>
        <div class="square "></div>
        <div class="square last"></div>
    </div>
</div>
<div class="contentBox" v-if="page==false">
  <RouterView />
</div>
<div class="contentBox1" v-else>
  <RouterView />
</div>
  </div>
</template>

<style scoped lang="scss">
.header {
  width: 100vmax;
  height: 8vh;
  position: fixed;
  top: 0px;
  z-index: 5;
}
.del{
  width: 100%;
  height: 8vmin;
  margin-bottom: 0px;
  background-color: #ACB1D6;
}
.content {
  margin-left: auto;
  padding-top: 0.1vmin;
  width: 200vmin;
  height: 200vmin;
  background-color: #512B81;
  .contentBox{
    margin-top: 8vmin;
  }
}
.content1 {
  margin-left: auto;
  padding-top: 0.1vmin;
  width: 181vmin;
  height: 200vmin;
  background-color: #512B81;
  .contentBox{
    margin-top: 10vmin;
  }
}

// 載入動畫
$squarew: 15px;
$squareh: 15px;
$squaremargin: 5px;
$loaderw: $squarew * 3 + $squaremargin *2;
$loaderh: $squareh * 3 + $squaremargin *2;
$delayenter: 0.3s;
$topenter: -10px;

@mixin transition($value) {
  -webkit-transition: $value ;
   -moz-transition: $value ;
          transition: $value ;
}

@mixin delay( $delay ) {
  -webkit-animation-delay: $delay;
   -moz-animation-delay: $delay;
  animation-delay: $delay;
}
@-webkit-keyframes enter{
  0%   { 
    opacity: 0;
    top: $topenter;
  }
  5%   { 
    opacity: 1;
    top: 0px;
  }
  50.9% { 
    opacity: 1;
    top: 0px;
  }
  55.9% { 
    opacity: 0;
    top: - $topenter;
  }
}
@keyframes enter{
  0%   { 
    opacity: 0;
    top: $topenter;
  }
  5%   { 
    opacity: 1;
    top: 0px;
  }
  50.9% { 
    opacity: 1;
    top: 0px;
  }
  55.9% { 
    opacity: 0;
    top: - $topenter;
  }
}
@-moz-keyframes enter{
  0%   { 
    opacity: 0;
    top: $topenter;
  }
  5%   { 
    opacity: 1;
    top: 0px;
  }
  50.9% { 
    opacity: 1;
    top: 0px;
  }
  55.9% { 
    opacity: 0;
    top: - $topenter;
  }
}


.loader{
    width: 200vmin;
    height: 100vmin;
    margin-left: auto;
  position: fixed;
  z-index: 4;
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
}
.square{
  background: white;
  width: $squarew;
  height: $squareh;
  float: left;
  top: $topenter;
  margin-right: $squaremargin;
  margin-top: $squaremargin;
  position:relative;
  opacity: 0;
  -webkit-animation: enter 6s infinite;
  animation: enter 6s infinite;
}
.enter{
  top: 0px;
  opacity: 1;
}
.square:nth-child(1){
  @include delay(6 * $delayenter);
}
.square:nth-child(2){
 @include delay(7 * $delayenter);
}
.square:nth-child(3){
  @include delay(8 * $delayenter);
  background: #fdc96f;
}
.square:nth-child(4){
  @include delay(3 * $delayenter);
}
.square:nth-child(5){
  @include delay(4 * $delayenter);
}
.square:nth-child(6){
  @include delay(5 * $delayenter);
}
// .square:nth-child(7){
//   }
.square:nth-child(8){
  @include delay(1 * $delayenter);
}
.square:nth-child(9){
  @include delay(2 * $delayenter);
}
.clear{
  clear: both;
 }
.last{
   margin-right:0;
}
.stop {
  .square {
    -webkit-animation: none; // 关闭动画
    animation: none; // 关闭动画
  }
}

@media screen and (max-width: 912px){
  .content{
    width: 90vmin;
  }
  .loader{
    width: 100vmin;
    height: 145vmin;
  }
}
@media screen and (max-width: 412px){
  .header{
    height: 9vmin;
  }
  .content{
    width: 100vmin;
    height: 214vmin;
  }
  .content1{
    margin-top: 9vmin;
    width: 75vmin;
    height: 214vmin;
  }
  .loader{
    width: 90vmin;
    height: 214vmin;
  }
}

</style>
