<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import TheWrapper from "./components/TheWrapper.vue";
import NavPanel from "@/components/NavPanel.vue";
import TheMenu from "@/components/TheMenu.vue";
</script>

<template>
<!--<TheWrapper>-->
<!--  <header>-->
<!--    <NavPanel/>-->
<!--&lt;!&ndash;    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />&ndash;&gt;-->

<!--&lt;!&ndash;    <div class="wrapper">&ndash;&gt;-->
<!--&lt;!&ndash;      <HelloWorld msg="You did it!" />&ndash;&gt;-->
<!--&lt;!&ndash;    </div>&ndash;&gt;-->
<!--  </header>-->

<!--  <main>-->
<!--&lt;!&ndash;    <TheWelcome />&ndash;&gt;-->
<!--  </main>-->
<!--</TheWrapper>-->
  <TheMenu/>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
