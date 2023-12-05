<script>

export default{
    data(){
        return{
            loader:"loader",
            stop:"stop"
        }
    },
    mounted(){
        setTimeout(()=>{
            this.loader=this.stop
        },5000)

    },
}



// let ddd=document.getElementById("ddd")
// ddd.addEventListener("click", ()=> {
//     console.log("123");
// });
function aaa(){
    
        let square=document.querySelector(".loader")
        square.classList
     // 5000毫秒 = 5秒
}

</script>

<template>
    <!-- <button id="ddd" @click="aaa()">123</button> -->

    <div class="example-1 card">
    <div class="wrapper">
      <!-- <div class="date">
        <span class="day">12</span>
        <span class="month">Aug</span>
        <span class="year">2016</span>
      </div> -->
      <div class="data">
        <div class="content">
          <span class="author">Jane Doe</span>
          <h1 class="title"><a href="#">Boxing icon has the will for a couple more fights</a></h1>
          <p class="text">The highly anticipated world championship fight will take place at 10am and is the second major boxing blockbuster in the nation after 43 years.</p>
          <!-- <label for="show-menu" class="menu-button"><span></span></label> -->
        </div>
        <!-- <input type="checkbox" id="show-menu" /> -->
        <!-- <ul class="menu-content">
          <li>
            <a href="#" class="fa fa-bookmark-o"></a>
          </li>
          <li><a href="#" class="fa fa-heart-o"><span>47</span></a></li>
          <li><a href="#" class="fa fa-comment-o"><span>8</span></a></li>
        </ul> -->
      </div>
    </div>
  </div>

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
  width: 40%;
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
    min-height: 540px;
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
    background: url(https://media.discordapp.net/attachments/483550384133111808/1166774573275029616/chihuahua-smile.gif?ex=654bb67f&is=6539417f&hm=78c84357c72c0e87d184405d55ab6b876b443a192adb97ad1e85f97f3715a7e1&) 20% 1% / cover no-repeat;
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
      color: lighten($black, 50%);
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

</style>
