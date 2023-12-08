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
          <!-- <span class="author">Jane Doe</span> -->
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

@import url(https://fonts.googleapis.com/css?family=Open+Sans:300,400,700);
// Variables
$regal-blue: #034378;
$san-juan: #2d4e68;
$bermuda: #77d7b9;
$white: #fff;
$black: #000;
$open-sans: 'Open Sans',
sans-serif;
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

h1 {
  font-family: $open-sans;
  font-weight: 300;
}

.row {
  max-width: 900px;
  margin: 50px auto 0;
}

// Base styles
.card {
  float: left;
  padding: 0 1.7rem;
  width: 108vmin;
  margin-left: 20vmin;
  margin-bottom: 20vmin;
  .menu-content {
    @include cf;
    margin: 0;
    padding: 0;
    list-style-type: none;
    li {
      display: inline-block;
    }
    a {
      color: $white;
    }
    span {
      position: absolute;
      left: 50%;
      top: 0;
      font-size: 10px;
      font-weight: 700;
      font-family: 'Open Sans';
      transform: translate(-50%, 0);
    }
  }
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
  .author {
    font-size: 12px;
  }
  .title {
    margin-top: 10px;
  }
  .text {
    height: 70px;
    margin: 0;
  }
  input[type='checkbox'] {
    display: none;
  }
  input[type='checkbox']:checked + .menu-content {
    transform: translateY(-60px);
  }
}

// First example styles
.example-1 {
  .wrapper {
    background-image: url(https://media1.tenor.com/m/1IMoSGd3FS4AAAAC/seal-sax.gif);
    background-repeat: no-repeat;
        background-size: 100%;
  }
  .date {
    position: absolute;
    top: 0;
    left: 0;
    background-color: $bermuda;
    color: $white;
    padding: 0.8em;
    span {
      display: block;
      text-align: center;
    }
    .day {
      font-weight: 700;
      font-size: 24px;
      text-shadow: 2px 3px 2px rgba($black, 0.18);
    }
    .month {
      text-transform: uppercase;
    }
    .month,
    .year {
      font-size: 12px;
    }
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
  .menu-button {
    position: absolute;
    z-index: 999;
    top: 16px;
    right: 16px;
    width: 25px;
    text-align: center;
    cursor: pointer;
    span {
      width: 5px;
      height: 5px;
      background-color: lighten($black, 50%);
      color: lighten($black, 50%);
      position: relative;
      display: inline-block;
      border-radius: 50%;
      &::after,
      &::before {
        content: '';
        display: block;
        width: 5px;
        height: 5px;
        background-color: currentColor;
        position: absolute;
        border-radius: 50%;
      }
      &::before {
        left: -10px;
      }
      &::after {
        right: -10px;
      }
    }
  }
  .menu-content {
    text-align: center;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    z-index: -1;
    transition: transform 0.3s;
    transform: translateY(0);
    li {
      width: 33.333333%;
      float: left;
      background-color: $bermuda;
      height: 60px;
      position: relative;
    }
    a {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 24px;
    }
    span {
      top: -10px;
    }
  }
}


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
	transition-delay: 400ms;
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
