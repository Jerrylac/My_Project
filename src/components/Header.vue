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
    <RouterLink to="/" class="link">
      <i class="fa-solid fa-house"></i>
    </RouterLink>
    <RouterLink to="/about" class="link">About</RouterLink>
    
  </div>
  <div class="left">


  </div>

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
    width: 5vw;
    height: 10vh;
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
    width: 5vw;
    height: 10vh;
    background-color: black;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0.1;
    .fa-bars{
      font-size: 45px;
    }
  }
  .fa-house {
    font-size: 50px;
    color: #6d5d6e;
}
}

.left{
  width: 10vmax;
  height: 100vh;
  background-color: black;
  position: fixed;
  z-index: 0;
}
</style>
