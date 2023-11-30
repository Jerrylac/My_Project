<script setup></script>

<template>
  <div class="flipBox">

    <div class="flip1">
      <div class="front" >
        <h1 class="text-shadow">關於我</h1>
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
  <div class="flipBoxT">
    <div class="flip">
      <div class="front" style="background-image: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif);">
        <h1 class="text-shadow">關於我</h1>
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
          background-image: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif);
        "
      >
        <h1 class="text-shadow">關於我</h1>
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
          background-image: url(https://media4.giphy.com/media/TcdpZwYDPlWXC/giphy.gif);
        "
      >
        <h1 class="text-shadow">關於我</h1>
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
  }
}
h1 {
  font-size: 2.2em;
  color: #000;
  text-shadow: 0px 0px 5px white;
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
      border-radius: 10px;
      p {
        font-size: 0.9125rem;
        line-height: 160%;
        color: #999;
      }
    }
  }

}
</style>
