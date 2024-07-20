<template>
  <div class="collection">
    <div class="collectionText">
      <h1>Collections</h1>
    </div>
    <div class="collectionCards">
      <CollectionCard v-for="item in nfts" :key="item.id" :nft="item" />
      <img
        src="../assets/slidderButtonleft.svg"
        alt="slidderleft"
        class="leftSlidder"
      />
      <img
        src="../assets/slidderButtonRight.svg"
        alt="slidderright"
        class="rightSlidder"
      />
    </div>
  </div>
</template>

<script>
import CollectionCard from "./CollectionCard.vue";

export default {
  name: "collection",
  data() {
    return {
      nfts: [
        {
          id: 1,
          name: "XO Girls NFT Collection",
          description: "Floor: 0.07 ETH ",
          image: require("@/assets/card1.png"),
        },
        {
          id: 2,
          name: "Game character 3d Collection",
          description: "Floor: 0.05 ETH ",
          image: require("@/assets/card2.png"),
        },
        {
          id: 3,
          name: "Monkey Collections",
          description: "Floor: 0.01 ETH ",
          image: require("@/assets/card3.png"),
        },
        {
          id: 4,
          name: "PROJECT NFT cub ",
          description: "Floor: 0.07 ETH ",
          image: require("@/assets/card4.png"),
        },
      ],
    };
  },
  components: {
    CollectionCard,
  },
};
</script>

<style>
.collection {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--background, #000);
  padding-top: 50px;
}
.collectionText {
  text-align: left;
  width: 100%;
}
.collectionText h1 {
  padding-left: 150px;
  color: #fff;
  font-family: Poppins;
  font-size: 40px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}
.collectionCards {
  margin-top: 50px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 24px;
  position: relative;
}

.leftSlidder {
  position: absolute;
  left: 0;
  transform: translate(-50%, -100%);
}
.rightSlidder {
  position: absolute;
  right: 0;
  transform: translate(50%, -100%);
}
@media (max-width: 1024px) {
  .collectionText h1 {
    padding-left: 20px;
    font-size: 32px;
    text-align: center;
  }

  .collectionCards {
    flex-direction: column;
    gap: 16px;
  }

  .leftSlidder,
  .rightSlidder {
    display: none; 
  }
}


@media (max-width: 768px) {
  .collectionText h1 {
    padding-left: 10px;
    font-size: 24px;
    text-align: center;
  }

  .collectionCards {
    margin-top: 30px;
    gap: 12px;
  }

  .leftSlidder,
  .rightSlidder {
    display: none;
  }
}
</style>
