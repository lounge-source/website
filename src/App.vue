<script setup>
import TheFoodMenu from "@/components/TheFoodMenu.vue";
import TheRules from "@/components/TheRules.vue";
import TheHookahMenu from "@/components/TheHookahMenu.vue";
</script>

<template>
  <div class="wrapper">
    <TheFoodMenu/>
    <TheHookahMenu/>
    <TheRules/>
  </div>

</template>

<style scoped>
.wrapper {
  width: 100%;
  min-height: 100vh;
  background: url("@/assets/images/background.png") repeat;
  font-family: "Roboto", serif;
  color: #d9d1c9;
  font-weight: 100;
  padding: 30px 150px 80px;
}

</style>
