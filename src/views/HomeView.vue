<script setup></script>

<template>
  <div class="flipBox">

    <div class="flip1">
      <div class="front" style="
          background-image: url(https://media.discordapp.net/attachments/483550384133111808/1166774573275029616/chihuahua-smile.gif?ex=654bb67f&is=6539417f&hm=78c84357c72c0e87d184405d55ab6b876b443a192adb97ad1e85f97f3715a7e1&);
        ">
        <h1 class="text-shadow">預定照片</h1>
      </div>
      <div class="back">
        <p>預定照片</p>
      </div>
    </div>
  </div>
  <div class="flipBoxT">
    <div class="flip">
      <div class="front" style="background-image: url();">
        <div class="userT">
          <i class="fa-solid fa-user-large"></i>
          <h1 class="text-shadow">關於我</h1>
        </div>
      </div>
      <div class="back">
        <h2>Angular</h2>
        <p>
          Good tools make application development quicker and easier to maintain
          than if you did everything by hand..
        </p>
      </div>
    </div>
    <div class="flip">
      <div class="front" style="">
        <div class="bockT">
          <i class="fa-brands fa-readme"></i>
          <h1 class="text-shadow">學習經歷</h1>
          
        </div>
      </div>
      <div class="back">
        <h2>Angular</h2>
        <p>
          Good tools make application development quicker and easier to maintain
          than if you did everything by hand..
        </p>
      </div>
    </div>
    <div class="flip">
      <div
        class="front"
        style="
          
        "
      >
      <div class="workI">

        <i class="fa-solid fa-briefcase"></i>
        <h1 class="text-shadow"> 工作經歷</h1>
      </div>
      </div>
      <div class="back">
        <h2>Angular</h2>
        <p>
          Good tools make application development quicker and easier to maintain
          than if you did everything by hand..
        </p>
      </div>
    </div>

  </div>
  
  <!-- <a href="https://mythrillfiction.com/" target="_blank">Mythrill</a> -->
</template>
<style scoped lang="scss">
  h1 {
    font-size: 2.2em;
    color: #000;
    text-shadow: 0px 0px 5px white;
  }
.flipBoxT{
  width: 100vw;
height: 100vmin;
// background-color: azure;
padding-left: 7vmin;
  .flip {
    margin-top: 50px;
    margin-left: 20vmin;
  
    position: relative;
    .front,
    .back {
      display: block;
      transition-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.275);
      transition-duration: 0.5s;
      transition-property: transform, opacity;
    }
    .front {
      transform: rotateY(0deg);
    }
    .back {
      position: absolute;
      opacity: 0;
      top: 0px;
      left: 0px;
      width: 100%;
      height: 100%;
      transform: rotateY(-180deg);
    }
    &:hover {
      .front {
        transform: rotateY(180deg);
      }
      .back {
        opacity: 1;
        transform: rotateY(0deg);
      }
    }
    &.flip-vertical {
      .back {
        transform: rotateX(-180deg);
      }
      &:hover {
        .front {
          transform: rotateX(180deg);
        }
        .back {
          transform: rotateX(0deg);
        }
      }
    }
  }
  .flip {
    position: relative;
    display: inline-block;
    width: 45vmin;
    .front,
    .back {
      box-shadow: 5px 5px 5px black;
      display: block;
      color: white;
      width: inherit;
      background-size: cover !important;
      background-position: center !important;
      height: 80vmin;
      padding: 1em 2em;
      background: #313131;
      border-radius: 10px;
      p {
        font-size: 0.9125rem;
        line-height: 160%;
        color: #999;
      }
    }
    .workI{
      margin-top: 50%;
      .fa-briefcase{
        font-size: 5vmin;
        display: flex;
        justify-content: center;
      }
      h1{
        margin-top: 20px;
        font-size: 2.2em;
        color: #000;
        text-align: center;
        text-shadow: 0px 0px 5px white;
      }
    }
    .bockT{
      margin-top: 50%;
      .fa-readme{
        font-size: 5vmin;
        display: flex;
        justify-content: center;
      }
      h1{
        margin-top: 20px;
        font-size: 2.2em;
        color: #000;
        text-align: center;
        text-shadow: 0px 0px 5px white;
      }
    }
    .userT{
      margin-top: 50%;
      .fa-user-large{
        font-size: 5vmin;
        display: flex;
        justify-content: center;
      }
      h1{
        margin-top: 20px;
        font-size: 2.2em;
        color: #000;
        text-align: center;
        text-shadow: 0px 0px 5px white;
      }
    }
  }
}

.flipBox{
  
  margin-left: 20vmin;
  width:200vmin;
  height: 60vmin;
  border-bottom: 2px solid black;
  // background-color: #fff;
  .flip1 {
    margin-top: 50px;
    margin-left: 10vmin;
  
    position: relative;
    .front,
    .back {
      display: block;
      transition-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.275);
      transition-duration: 0.5s;
      transition-property: transform, opacity;
    }
    .front {
      transform: rotateY(0deg);
    }
    .back {
      position: absolute;
      opacity: 0;
      top: 0px;
      left: 0px;
      width: 100%;
      height: 100%;
      transform: rotateY(-180deg);
    }
    &:hover {
      .front {
        transform: rotateY(180deg);
      }
      .back {
        opacity: 1;
        transform: rotateY(0deg);
      }
    }
    &.flip-vertical {
      .back {
        transform: rotateX(-180deg);
      }
      &:hover {
        .front {
          transform: rotateX(180deg);
        }
        .back {
          transform: rotateX(0deg);
        }
      }
    }
  }
  .flip1 {
    position: relative;
    display: inline-block;
    width: 45vmin;
    .front,
    .back {
      box-shadow: 5px 5px 5px black;
      display: block;
      color: white;
      width: inherit;
      background-size: cover !important;
      background-position: center !important;
      height: 40vmin;
      padding: 1em 2em;
      background: #313131;
      border-radius: 50%;
      p {
        font-size: 0.9125rem;
        line-height: 160%;
        color: #999;
      }
    }
  }

}
</style>
