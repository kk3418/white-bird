<script setup></script>
<template>
  <div class="container"></div>
</template>
<style scoped>
.container {
  width: 5vw;
  height: 5vw;
  position: absolute;
  left: 21.5vw;
  border-radius: 50%;
  box-shadow: 0 0 0.375rem 0 #00000040;
  background-color: #fff;
  z-index: 10;
}
@media (max-width: 750px) {
  .container {
    width: 13vw;
    height: 13vw;
    left: unset;
    right: 7vw;
  }
}
</style>
