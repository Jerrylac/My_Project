<script setup></script>

<template>
  <div class="imgBox">
    <img
      src="https://media.discordapp.net/attachments/853004774487097344/1096814329975804004/ezgif.com-gif-maker.gif"
      alt="a random girl"
    />
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

  <!-- <a href="https://mythrillfiction.com/" target="_blank">Mythrill</a> -->
</template>
<style scoped lang="scss">
@property --h {
  syntax: "<percentage>";
  initial-value: 0%;
  inherits: true;
}
.imgBox {
  width: 95vmax;
  height: 50vmin;
  margin-left: 5vmin;
  border-bottom: 1px solid black;
  img {
    margin-top: 30px;
    margin-left: 50px;
    margin-bottom: 50px;
    --b: 15px; /* border width */
    --g: 10px; /* gap */

    width: 250px;
    object-fit: cover;
    border-radius: 10px;
    // border-radius: 50%;
    padding: calc(var(--b) + var(--g));
    background: conic-gradient(from 180deg in oklch longer hue, red 0 0);
    -webkit-mask: radial-gradient(
        farthest-side,
        #000 calc(100% - var(--b) - var(--g) - 1px),
        /* #0000 calc(100% - var(--b) - var(--g)) 
              calc(100% - var(--b)),*/
          #000 calc(100% - var(--b) + 1px)
      ),
      conic-gradient(
        from 180deg,
        #0000 calc(var(--p) - var(--h)),
        #000 0 var(--p),
        #000 0 calc(var(--p) + var(--h)),
        #0000 0
      ),
      linear-gradient(#000 0 0) content-box;
    -webkit-mask-composite: source-in, destination-over;
    mask-composite: intersect, add;
    --p: 0%;
    transition: --h 0.5s linear, scale 0.5s;
    cursor: pointer;
  }
  img:hover {
    --h: 100%;
    --p: 100%;
    scale: 1.1;
  }
}

h1 {
  font-size: 2.2em;
  color: #000;
  text-shadow: 0px 0px 5px white;
}
.flip {
  margin-top: 50px;
  margin-left: 10%;

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
  width: 300px;
  .front,
  .back {
    box-shadow: 5px 5px 5px black;
    display: block;
    color: white;
    width: inherit;
    background-size: cover !important;
    background-position: center !important;
    height: 520px;
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
</style>
