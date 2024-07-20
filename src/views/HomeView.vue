<template>
<div class="pageContainer">

<WelcomeSection/>
  <NFT/>
  <Collection/>
  <Footer/>
</div>

</template>

<script>
import Collection from './Collection.vue';
import Footer from './Footer.vue';
import NFT from './NFT.vue';
import WelcomeSection from './welcomeSection.vue';



export default {
  name: "HomeView",
  components: {NFT,WelcomeSection,Collection,Footer},
};
</script>
<style>
*{
  margin: 0;
  padding: 0;
}

.pageContainer{
  width: 100vw;
  margin: 0px;
  padding: 0px;

}
</style>
