<script>
import "@fontsource/open-sans"
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue'
export default {
  components: { AppHeader, AppMain, AppFooter },
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Open Sans Condensed", sans-serif;
}

.container {
  margin: 0 auto;
  width: 1250px;
}

.active {
  color: dodgerblue;
  border-bottom: 4px solid dodgerblue;
}
</style>
