<template>
  <div class="slider">
    <div class="sliderContent">
      <h2>Powering leading brands</h2>
      <img src="../assets/sliderLogo.svg" alt="sliderlogo" />
      <img src="../assets/sliderLogo2.png" alt="sliderlogo2" />
    </div>
  </div>
  <div>
    <NFTCard v-for="item in nfts" :key="item.id"  :nft="item"/>
  </div>
</template>

<script>
import NFTCard from "./NFTCard.vue";
export default {
  name: "NFT",
  data() {
    return {
      nfts: [
        {
          id: 1,
          name: "Moddy Character NFT",
          description:
            "The image is a high-quality digital painting with a resolution of 3000x2000 pixels and is optimized for the web.",
          price: "$101,593",
         image: require('@/assets/nft1.png'),
          isRight: true,
           className:"nft-card"
        },
        {
          id: 2,
          name: "KattyEfa NFT",
          description:
            "The image is a high-quality digital painting with a resolution of 5000x1250 pixels.",
          price: "$1.5 million",
            image: require('@/assets/nft2.png'),
          isRight: false,
          className:"reverse"
        },
      ],
    };
  },
  components: {
    NFTCard,
  },
};
</script>

<style>
.slider {
  width: 100vw;
  height: 83px;
  background: var(--second, rgba(129, 103, 151, 0.7));
  text-align: center;
  display: flex;
  flex-direction: row;
  justify-items: center;
  align-items: center;
}
.sliderContent {
  margin: 0px;
  padding: 0px;
  display: flex;
  flex-direction: row;
  justify-items: center;
  align-items: center;
  gap: 202px;
  width: 80%;
  margin: 0 auto;
}
.sliderContent h2 {
  color: #fff;
  font-family: Poppins;
  font-size: 32px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
height: fit-content; 
 white-space: nowrap;
  
  
  
}

@media (max-width: 1024px) {
  .slider{
    height: 100%;
    padding: 40px 0;
  }
  .sliderContent {
    display: flex;
    flex-direction: column;
    gap: 30px;

  }

  .sliderContent h2 {
    font-size: 28px;
    width: 50%;
     white-space: wrap;
  }
  .sliderContent img{
    width: 50%;
  }
}

@media (max-width: 768px) {
  .sliderContent {
    flex-direction: column;
    gap: 20px;
  }

  .sliderContent h2 {
    font-size: 24px;
    width: 50%;
  }

  .sliderContent img {
    width: 50%;
  }
}

@media (max-width: 480px) {
  .sliderContent {
    gap: 10px;
  }

  .sliderContent h2 {
    font-size: 20px;
  }

  .sliderContent img {
    width: 70%;
  }
}
</style>
