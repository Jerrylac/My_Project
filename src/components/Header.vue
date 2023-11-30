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
    <i class="fa-solid fa-bars"></i>
    <RouterLink to="/" class="link"
      ><i class="fa-solid fa-house"></i
    ></RouterLink>
    <RouterLink to="/about" class="link">About</RouterLink>
    
  </div>
</template>

<style scoped lang="scss">
.headerShow {
  width: 100%;
  height: 100%;
  background-color: #DBDFEA;
  font-size: 30px;
}
// a{
//     margin-top: 500px;
// }
.fa-house {
  margin-top: 20px;
  font-size: 50px;
  color: #6d5d6e;
}
.fa-bars{
  font-size: 50px;
  margin-top: 25px;
  margin-left: 30px;
}
a.router-link-exact-active {
  color: #3e065f;
  font-weight: bold;
  background-color: #f4eee0;
  box-shadow: 3px 5px 1px black;
}


</style>
