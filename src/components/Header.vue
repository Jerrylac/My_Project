<script>
import { RouterLink, RouterView } from "vue-router";
export default {
  data() {
    return {
      page:false
    };
  },
  components: {
    RouterLink,
  },
  methods:{
    chPage(){
      if(this.page==false){
        this.page=true
        this.$emit("pageCh",this.page)
      }else{
        this.page=false
        this.$emit("pageCh",this.page)
      }
    }
  }
};
</script>

<template>
  <div class="headerShow">
    <div class="faBox" @click="chPage">
      <i class="fa-solid fa-bars"></i>
    </div>
    <!-- <div class="vBox">
      <div class="line-container">
        <div class="colorful-line" style="--i: 4"></div>
        <div class="colorful-line" style="--i: 8"></div>
        <div class="colorful-line" style="--i: 1"></div>
        <div class="colorful-line" style="--i: 3"></div>
        <div class="colorful-line" style="--i: 7"></div>
        <div class="colorful-line" style="--i: 2"></div>
        <div class="colorful-line" style="--i: 5"></div>
        <div class="colorful-line" style="--i: 6"></div>
      </div>
    </div> -->
    
    
  </div>
  <div class="left" v-if="page==false">
    <div class="box1">
      <RouterLink to="/" class="link">
        <i class="fa-solid fa-house"></i>
        <!-- <p>首頁</p> -->
      </RouterLink>
    </div>
    <div class="box1">
      <RouterLink to="/about" class="link">
        <i class="fa-solid fa-wand-magic-sparkles"></i>
        <!-- <p>作品</p> -->
      </RouterLink>
    </div>
    <!-- <div class="box1">
      <RouterLink to="/test" class="link">
        <i class="fa-solid fa-wand-magic-sparkles"></i>
        <p>作品</p>
      </RouterLink>
    </div> -->
    

  </div>
  <div class="left-bg" v-else>
    <div class="box1">
      <RouterLink to="/" class="link">
        <i class="fa-solid fa-house"></i>
      </RouterLink>
      <p>首頁</p>
    </div>
    <div class="box1">
      <RouterLink to="/about" class="link">
        <i class="fa-solid fa-wand-magic-sparkles"></i>
      </RouterLink>
      <p>作品</p>
    </div>
  </div>

<!-- <RouterLink to="/Accountinglogin" class="link">記帳</RouterLink> -->
</template>

<style scoped lang="scss">
.headerShow {
  width: 100%;
  height: 100%;
  background-color: #35155D;
  font-size: 30px;
  display: flex;
  align-items: center;
  padding-top: 10px;
    padding-left: 30px;
  .faBox{
    width: 7vmin;
    height: 6vmin;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    .fa-bars{
      font-size: 6vmin;
      display: flex;
      justify-content: center;
      align-items: center;
      // margin-top: 25px;
      // margin-left: 30px;
    }
  }
  .faBox:hover{
    width: 7vmin;
    height: 6vmin;
    background-color: black;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0.5;
    .fa-bars{
      font-size: 5vmin;
    }
  }
  .vBox{
    // width:30vmin;
    // height: 2vmin;
    // background-color: #000;
    margin-top: 2vmin;
    margin-left: 180vmin;
    .line-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 20vmin;
  height: 20vmin;
  // background-color: #fff;
}

.colorful-line {
  width: 4vmin;
  border-radius: 10px;
  box-shadow: 2px 2px 10px 2px rgba(0, 0, 0, 0.4);
  transform: scale(1);
  transition: transform 0.2s;
  animation: flow 4s infinite cubic-bezier(0, 0.57, 1, 0.46);
  animation-delay: calc(-0.5s * var(--i));
}

.colorful-line:hover {
  transform: scale(1.3);
}

.colorful-line:nth-child(1) {
  background-color: rgb(250, 215, 220);
}

.colorful-line:nth-child(2) {
  background-color: rgb(215, 236, 250);
}

.colorful-line:nth-child(3) {
  background-color: rgb(223, 215, 250);
}

.colorful-line:nth-child(4) {
  background-color: rgb(250, 215, 249);
}

.colorful-line:nth-child(5) {
  background-color: rgb(245, 250, 215);
}

.colorful-line:nth-child(6) {
  background-color: rgb(218, 250, 215);
}

.colorful-line:nth-child(7) {
  background-color: rgb(215, 220, 250);
}

.colorful-line:nth-child(8) {
  background-color: rgb(250, 215, 249);
}

@keyframes flow {
  0%,
  100% {
    height: 20%;
    border-radius: 5px;
  }
  50% {
    height: 50%;
    border-radius: 30px;
  }
}
  }
}

.left{
  width: 7vmax;
  height: 100vmin;
  background-color:#35155D;
  border-top: 3px solid black;
  position: fixed;
  font-size: 30px;
  z-index: 0;
  .box1{
    width: 100%;
    margin-top: 20%;
    
    .fa-wand-magic-sparkles{
      margin-top: 5%;
      margin-left: 10%;
      font-size: 6vmin;
      color: #F0ECE5;
    }
    .fa-house {
      margin-top: 5%;
      margin-left: 10%;
      font-size: 6vmin;
      color: #F0ECE5;
    }&:hover{
    opacity: 0.5;
  }
    p{

      font-size: 20px;
    }
  }
}
.left-bg{
  width: 15vmax;
  height: 100vh;
  background-color:#35155D;
  border-top: 3px solid black;
  position: fixed;
  font-size: 30px;
  z-index: 0;
  .box1{
    width: 100%;
    margin-top: 20%;
    display: flex;
    cursor: pointer;
    // background-color:black;
    .link{
      margin-top: 0px;
      margin-left: 0px;
      width: 50%;
      height: 100%;
    }
    .fa-wand-magic-sparkles{
      margin-top: 5%;
      margin-left: 10%;
      font-size: 6vmin;
      color: #F0ECE5;
    }
    .fa-house {
      margin-top: 5%;
      margin-left: 10%;
      font-size: 6vmin;
      color: #F0ECE5;
    }&:hover{
    opacity: 0.5;
  }
    p{
      margin-top: 10px;
      cursor: pointer;
      font-size: 5vmin;
    }
  }
}

@media screen and (max-width: 912px){
  .headerShow{
    padding-left: 2vmin;
  }
  .left{
    width: 10vmin;
    height: 300vmin;
  }
  .left-bg{
    height: 160vmin;
    .box1{
      p{
        font-size: 4vmin;
      }
    }
  }
}

@media screen and (max-width: 440px){
  .headerShow{
    width: 100vmin;
    height: 10vmin;
    padding-left: 2vmin;
  }
  .left{
    width: 10vmin;
    height: 220vmin;
  }
  .left-bg{
    height: 210vmin;
  }
}

</style>
