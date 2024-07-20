<template>
    <div class="home">
    <div class="homeContent">
      <div class="upperContent">
        <h1>Your own NFT Market place without Coding</h1>
        <p>
          The fastest and easiest way to fully unlock the potential of your
          digital assets. Create and run an exclusive marketplace for your NFT
          business today!
        </p>
      </div>
      <div class="formContent">
        <input type="text" value="Enter your email...." />
        <button>Start Free</button>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {

}
</script>
<style>
.home {
  margin: 0px;
  padding: 0px;
  width: 100vw;
  height: 100vh;
  background: url("../assets/homeBackground.png") no-repeat center center /
    cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.homeContent h1 {
  width: 677px;
  height: 122px;
  flex-shrink: 0;
  color: #fff;
  text-align: center;
  font-family: Poppins;
  font-size: 48px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.homeContent p {
  width: 497px;
  height: 67px;
  flex-shrink: 0;
  color: #fff;
  text-align: center;
  font-family: Poppins;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.upperContent {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 40px;
  margin-bottom: 44px;
}

.formContent {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 8px;
}

.formContent input {
  width: 272px;
  height: 40px;
  flex-shrink: 0;
  border-radius: 16px;
  opacity: 0.7;
  background: var(--background, #000);
  backdrop-filter: blur(10px);
  border: none;
  color: var(--text-color, #d6d5a8);
  font-family: Poppins;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  padding-left:24px  ;
}

.formContent button {
  width: 106px;
  height: 40px;
  flex-shrink: 0;
  border-radius: 16px;
  background: var(--help-color, rgba(82, 5, 123, 0.7));
  backdrop-filter: blur(10px);
  color: #fff;
  text-align: center;
  font-family: Poppins;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  border: none;
  outline: none;
  cursor: pointer;
}
@media (max-width: 1024px) {
  .upperContent{
    margin-top:350px;
  }
  .homeContent h1 {
    width: 80%;
    font-size: 36px;
  }

  .homeContent p {
    width: 70%;
    font-size: 14px;
  }

  .formContent {
    flex-direction: column;
    gap: 16px;
  }

  .formContent input, .formContent button {
    width: 80%;
  }
}

@media (max-width: 768px) {

  .homeContent h1 { 
    margin-top:50px ;
    width: 90%;
    font-size: 28px;
  }

  .homeContent p {
    width: 80%;
    font-size: 12px;
  }

  .formContent input, .formContent button {
    width: 90%;
  }
}

@media (max-width: 480px) {
  .homeContent h1 {
    width: 95%;
    font-size: 24px;
  }

  .homeContent p {
    width: 90%;
    font-size: 10px;
  }

  .formContent input, .formContent button {
    width: 95%;
  }
}

</style>