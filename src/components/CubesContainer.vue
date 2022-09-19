<template>
  <div class="cubes-container">
    <div class="cube cube-1"></div>
    <div class="cube cube-2"></div>
    <div class="cube cube-3"></div>
    <div class="cube cube-4"></div>
    <div class="cube cube-5"></div>
  </div>
</template>

<script>
export default {
  name: 'CubesContainer'
}
</script>

<style scoped>
.cubes-container {
  position: absolute;
  width: 100%;
  height: 100%;
  inset: 0;
  overflow: hidden;
  z-index: 0;
}

.cubes-container .cube {
  position: absolute;
  bottom: -32rem;
  width: 8rem;
  height: 8rem;
  border-radius: 0.4rem;
  background-color: rgba(255, 255, 255, 0.1);
  animation: rise 50s infinite;
}

.cubes-container .cube-1 {
  width: 16rem;
  height: 16rem;
  left: 20%;
  animation-duration: 34s;
  animation-delay: 2s;
}

.cubes-container .cube-2 {
  width: 8rem;
  height: 8rem;
  left: 25%;
  animation-duration: 34s;
  animation-delay: 4s;
}

.cubes-container .cube-3 {
  width: 12rem;
  height: 12rem;
  left: 40%;
  animation-duration: 44s;
  animation-delay: 4s;
}

.cubes-container .cube-4 {
  width: 24rem;
  height: 24rem;
  left: 70%;
  animation-duration: 44s;
  animation-delay: 3s;
}

.cubes-container .cube-5 {
  width: 32rem;
  height: 32rem;
  left: 90%;
  animation-duration: 40s;
  animation-delay: 22s;
}
@keyframes rise {
  0% {
    transform: translateY(0);
  }

  100% {
    transform: translateY(-150rem) rotate(600deg);
  }
}
</style>
