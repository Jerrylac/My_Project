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
}
.fa-house {
  font-size: 50px;
  color: #6d5d6e;
}
// a{
//     margin-top: 500px;
// }
// a.router-link-exact-active {
//   color: #3e065f;
//   font-weight: bold;
//   background-color: #f4eee0;
//   box-shadow: 3px 5px 1px black;
// }


</style>
