<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue';
</script>

<template>
      <div class="header">
        <Header/>
      </div>
      <div class="content">
        <RouterView />
      </div>
</template>

<style scoped lang="scss">
.header{
  width: 100vmax;
  height: 15vh;
}
.content{
  width: 100vmax;
  height: 85vmax;
  background-color: #393646;

}
</style>
