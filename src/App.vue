<template>
  <div id="app">
    <Navbar />
  
    <router-view />
  </div>
</template>

<script>
import Navbar from "./views/Navbar.vue";
import WelcomeSection from "./views/welcomeSection.vue";
import NFT from "./views/NFT.vue";

export default {
  name: "App",
  components: {
    Navbar,
    WelcomeSection,
    NFT,
  },
};
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
}
#app {
  margin: 0px;
  padding: 0px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-sizing: border-box;
  overflow: hidden;
}
</style>
