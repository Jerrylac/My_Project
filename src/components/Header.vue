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
  .left{
    width: 10vmin;
    height: 150vmin;
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

</style>
