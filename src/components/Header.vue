<script>
import { RouterLink, RouterView } from "vue-router";
export default {
  data() {
    return {};
  },
  components: {
    RouterLink,
  },
};
</script>

<template>
  <div class="headerShow">
    <div class="faBox">
      <i class="fa-solid fa-bars"></i>
    </div>
    
    
  </div>
  <div class="left">
    <div class="box1">
      <RouterLink to="/" class="link">
        <i class="fa-solid fa-house"></i>
        <p>首頁</p>
      </RouterLink>
    </div>
    <div class="box1">
      <RouterLink to="/about" class="link">About</RouterLink>
    </div>
    

  </div>

<!-- <RouterLink to="/Accountinglogin" class="link">記帳</RouterLink> -->
</template>

<style scoped lang="scss">
.headerShow {
  width: 100%;
  height: 100%;
  background-color: #DBDFEA;
  font-size: 30px;
  display: flex;
  align-items: center;
  padding-top: 10px;
    padding-left: 30px;
  .faBox{
    width: 3vw;
    height: 7vh;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    .fa-bars{
      font-size: 50px;
      display: flex;
      justify-content: center;
      align-items: center;
      // margin-top: 25px;
      // margin-left: 30px;
    }
  }
  .faBox:hover{
    width: 3vw;
    height: 6vh;
    background-color: black;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0.1;
    .fa-bars{
      font-size: 35px;
    }
  }
  
}

.left{
  width: 10vmax;
  height: 100vh;
  background-color: rgb(91, 86, 86);
  position: fixed;
  font-size: 30px;
  z-index: 0;
  .box1{
    width: 100%;
    margin-top: 20%;
    
    .fa-house {
      margin-top: 5%;
      margin-left: 10%;
      font-size: 40px;
      color: #F0ECE5;
    }&:hover{
    opacity: 0.5;
  }
    p{

      font-size: 20px;
    }
  }
}

</style>
