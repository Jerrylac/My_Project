<script>

export default{
    data(){
        return{

            }
    },
    methods:{
        gotest(){
            this.$router.push('/homeWork')
        },
        gotest1(){
            this.$router.push('/homeWork1')
        }
    }
    
}

</script>

<template>



    <div class="example-1 card">
    <div class="wrapper">
      <div class="data">
        <div class="content">
          <h1 class="title"><a href="https://joyful-frangipane-5bec0b.netlify.app/" target="_blank">上課操作連結</a></h1>
          
        </div>
      </div>
    </div>
  </div>


<!-- <div class="arrBox"> -->
  <div class="container">
	<div class="box box-1" style="--img: url(https://media1.tenor.com/m/4kyfWW2ktHcAAAAd/monkey-animal.gif);" data-text="找質數" @click="gotest()"></div>
	<div class="box box-2" style="--img: url(https://media1.tenor.com/m/uYr_ayFCAroAAAAd/math-raccoon.gif);" data-text="猜數字" @click="gotest1()"></div>
	<div class="box box-3" style="--img: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif
);" data-text="更新中.."></div>
	<div class="box box-4" style="--img: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif);" data-text="更新中.."></div>
	<div class="box box-5" style="--img: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif);" data-text="更新中.."></div>
</div>
<!-- </div> -->



</template>

<style scoped lang="scss">
// Variables

$white: #fff;
$black: #000;
// clear-fix mixin
@mixin cf {
  &::before,
  &::after {
    content: '';
    display: table;
  }
  &::after {
    clear: both;
  }
}
a {
  text-decoration: none;
}

// Base styles
.card {
  float: left;
  padding: 0 1.7rem;
  width: 108vmin;
  margin-left: 20vmin;
  margin-bottom: 20vmin;
  .wrapper {
    background-color: $white;
    width: 100vmin;
    height: 60vmin;
    position: relative;
    overflow: hidden;
    box-shadow: 0 19px 38px rgba($black, 0.3), 0 15px 12px rgba($black, 0.2);
    &:hover {
      .data {
        transform: translateY(0);
      }
    }
  }
  .data {
    position: absolute;
    bottom: 0;
    width: 100%;
    transform: translateY(calc(70px + 1em));
    transition: transform 0.3s;
    .content {
      padding: 1em;
      position: relative;
      z-index: 1;
    }
  }
  .title {
    margin-top: 10px;
  }
}

// First example styles
.example-1 {
  .wrapper {
    background-image: url(https://media1.tenor.com/m/qpJ2CXXlE3QAAAAC/%E9%87%8E%E7%8D%A3%E5%85%88%E8%BC%A9-%E5%88%9D%E6%97%A5%E3%81%AE%E5%87%BA%E5%85%88%E8%BC%A9.gif);
    background-repeat: no-repeat;
        background-size: 100%;
  }
  .content {
    background-color: $white;
    box-shadow: 0 5px 30px 10px rgba($black, 0.3);
  }
  .title {
    a {
      color:#35155D;
    }
  }
}
//-----------------------------

.container {
	position: relative;
	display: grid;
	grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
	gap: 1em;
	width: 800px;
	height: 500px;
	transition: all 400ms;
}

.container:hover .box {
	filter: grayscale(100%) opacity(24%);
}

.box {
	position: relative;
	background: var(--img) center center;
	background-size: cover;
	transition: all 400ms;
	display: flex;
	justify-content: center;
	align-items: center;
  cursor: pointer;
}

.container .box:hover {
	filter: grayscale(0%) opacity(100%);
}

.container:has(.box-1:hover) {
	grid-template-columns: 3fr 1fr 1fr 1fr 1fr;
}

.container:has(.box-2:hover) {
	grid-template-columns: 1fr 3fr 1fr 1fr 1fr;
}

.container:has(.box-3:hover) {
	grid-template-columns: 1fr 1fr 3fr 1fr 1fr;
}

.container:has(.box-4:hover) {
	grid-template-columns: 1fr 1fr 1fr 3fr 1fr;
}

.container:has(.box-5:hover) {
	grid-template-columns: 1fr 1fr 1fr 1fr 3fr;
}

.box:nth-child(odd) {
	transform: translateY(-16px);
}

.box:nth-child(even) {
	transform: translateY(16px);
}

.box::after {
	content: attr(data-text);
	position: absolute;
	bottom: 20px;
	background: #000;
	color: #fff;
	padding: 10px 10px 10px 14px;
	letter-spacing: 4px;
	text-transform: uppercase;
	transform: translateY(60px);
	opacity: 0;
	transition: all 400ms;
}

.box:hover::after {
	transform: translateY(0);
	opacity: 1;
	transition-delay: 50ms;
}



@media screen and (max-width: 912px){
  .card{
    width: 67vmin;
    margin-left: 2vmin;
    .wrapper{
        margin-top: 1vmin;
        width:  60vmin;
        height: 40vmin;
      }
      .content{

      }
  }
}
@media screen and (max-width: 440px){
  .card{
    width: 63vmin;
    margin-left: 1vmin;
    .wrapper{
      width:  50vmin;
      height: 40vmin;
      margin-left: 0px;
      background-size: 100%;
    }
    .content{
      height: 15vmin;
      a{
        font-size: 5vmin;
      }
    }
  }
}
</style>
