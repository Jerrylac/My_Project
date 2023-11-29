<script setup>

</script>

<template>
  <img src="https://media.discordapp.net/attachments/853004774487097344/1096814329975804004/ezgif.com-gif-maker.gif" alt="a random girl">

  
  
</template>
<style scoped lang="scss">
@property --h {
  syntax: "<percentage>";
  initial-value: 0%;
  inherits: true;
}

img {
  --b: 15px; /* border width */
  --g: 10px; /* gap */
  --c: red;
  
  width: 250px;
  aspect-ratio: 1;
  object-fit: cover;
  border-radius: 50%;
  padding: calc(var(--b) + var(--g));
  background: conic-gradient(from 180deg in oklch longer hue, red 0 0);
  -webkit-mask:
    radial-gradient(farthest-side,
      #000  calc(100% - var(--b) - var(--g) - 1px),
      #0000 calc(100% - var(--b) - var(--g)) 
            calc(100% - var(--b)),
      #000  calc(100% - var(--b) + 1px)),
    conic-gradient(from 180deg,
     #0000   calc(var(--p) - var(--h)),
     #000  0 var(--p),
     #0000,
     #000  0 calc(var(--p) + var(--h)),
     #0000 0),
    linear-gradient(#000 0 0) content-box;
  -webkit-mask-composite: source-in,destination-over;
          mask-composite: intersect,add;
  --p: 0%;
  transition: --h .5s linear,scale .5s;
  cursor: pointer;
}
img:hover {
  --h: 100%;
  --p: 100%;
  scale: 1.1;
}



</style>