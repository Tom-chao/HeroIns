<template>
  <div id="app">
    <CubesContainer />
    <ContainerAll />
  </div>
</template>
<script>
import CubesContainer from './components/CubesContainer.vue'
import ContainerAll from './components/ContainerAll.vue'
export default {
  name: 'app',
  components: { CubesContainer, ContainerAll }
}
</script>
<style scoped></style>
