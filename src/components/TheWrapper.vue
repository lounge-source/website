<template>
  <div class="wrapper">
    <div class="overlay"></div>

    <div class="content">
      <h1 class="title">FEARLounge</h1>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  position: relative;
  width: 100%;
  min-height: 100vh;
  background: url(src/assets/images/bar.jpg) no-repeat center center;
  background-size: cover;
  overflow: hidden;
  padding: 80px;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.7);
}

.content {
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  color: #fff;
  text-align: center;
  padding: 2rem;
}

.title {
  font-size: 22rem;
  margin-bottom: 1rem;
  color: transparent;
  -webkit-text-stroke: 1px white;
  opacity: 0.3;
  font-family: sans-serif;
}

</style>
<script setup>
</script>