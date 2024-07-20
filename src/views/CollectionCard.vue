<template>
  <div class="CardContainer">
    <div class="collection-image">
      <img :src="nft?.image" :alt="nft?.name" />
        <div class="collection-info">
      <h2>"{{ nft?.name }}"</h2>
      <p>{{ nft?.description }}</p>
    </div>
    </div>  
  </div>
</template>

<script>
export default {
  name: "CollectionCard",
  props: {
    nft: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
.collection-image img {
  padding: 0px;
  margin: 0px;
  width: 100%;
  height: 314px;

}
.collection-image{  position: relative;}
.collection-info {
  border-radius: 0px 0px 16px 16px;
  background: rgba(0, 0, 0, 0.5);
  width: 315px;
  height: 66px;
  flex-shrink: 0;
  color: white;
  position: absolute;
bottom: 0   ;

}

.collection-info h2 {
  color: #fff;
  text-align: center;
  font-family: Poppins;
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.collection-info p {
  color: #fff;
  text-align: center;
  font-family: Poppins;
  font-size: 15px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.CardContainer{
    height: 50vh;
}
</style>
