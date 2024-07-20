<template>
  <div :class="nft.className">
    <div class="nft-image">
      <img :src="nft?.image" :alt="nft?.name" />
    </div>
    <div class="nft-info">
      <h2>"{{ nft?.name }}"</h2>
      <p>{{ nft?.description }}</p>
      <span class="price">{{ nft?.price }}</span>
       <img src="../assets/rightArrow.svg" alt="arrow">
    </div>
  </div>
</template>

<script>
export default {
  name: 'NFTCard',
  props: {
    nft: {
      type: Object,
      required: true
    }
  }
};
</script>

<style scoped>
.nft-card {
    width: 100%;
    height: 80vh;
  display: flex;
  flex-direction: row-reverse;
  align-items: center;
  justify-content: center;
 

gap: 164px;
  background-color: #121212;
  color: #fff;
  border-bottom: 8px solid rgba(129, 103, 151, .7);
}
.reverse{
    width: 100%;
    height: 80vh;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  border-radius: 8px;
gap: 164px;
  background-color: #121212;
    border-bottom: 8px solid rgba(129, 103, 151, .7);
  color: #fff;}

.nft-image img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  
}

.nft-info {
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
margin-bottom: 50px;


}
.nft-info p{
    color: #FFF;
font-family: Poppins;
font-size: 32px;
font-style: normal;
font-weight: 400;
line-height: normal;
width: 465px;
flex-shrink: 0;
}

.price {
color: #FFF;
font-family: Poppins;
font-size: 32px;
font-style: normal;
font-weight: 700;
line-height: normal;
}
h2{
    color: #FFF;
font-family: Poppins;
font-size: 32px;
font-style: normal;
font-weight: 400;
line-height: normal;
}
.nft-info img{
    width: 69px;
height: 69px;
flex-shrink: 0;
margin-top:24px ;
}
@media (max-width: 1024px) {
  .nft-card,
  .reverse {
    padding-top:50px ;
    flex-direction: column;
    height: auto;
    gap: 20px;
  }

  .nft-info p,
  .price,
  h2 {
    font-size: 24px;
    text-align: center;
    width: 100%;
  }

  .nft-info img {
    width: 50px;
    height: 50px;
  }
}

@media (max-width: 768px) {
  .nft-card,
  .reverse {
    flex-direction: column;
    height: auto;
    gap: 16px;
  }

  .nft-info p,
  .price,
  h2 {
    font-size: 20px;
    text-align: center;
    width: 100%;
  }

  .nft-info img {
    width: 40px;
    height: 40px;
  }
}

@media (max-width: 480px) {
  .nft-card,
  .reverse {
    flex-direction: column;
    height: auto;
    gap: 10px;
  }

  .nft-info p,
  .price,
  h2 {
    font-size: 16px;
    text-align: center;
    width: 100%;
  }

  .nft-info img {
    width: 30px;
    height: 30px;
  }
}
</style>
