<template>
  <div class="footerContainer">
    <div class="upperFooter">
      <div class="footerForm">
        <h1>Join our weekly digest!</h1>
        <p>Get exclusive promotions & updates straight to your inbox.</p>
        <div class="emailSub">
          <input type="mail" placeholder="Enter your email...." />
          <button>Subscribe</button>
        </div>
        <button class="createButton">Create Free Store</button>
      </div>
      <div class="footerList">
        <div class="list">
          <h3>FEATURES</h3>
          <ul>
            <li>Build Store</li>
            <li>Sell NFT</li>
            <li>Grow Business</li>
          </ul>
        </div>
        <div class="list">
          <h3>SERVICES</h3>
          <ul>
            <li>Concierge</li>
            <li>Customization</li>
          </ul>
        </div>
        <div class="list">
          <h3>PRODUCT</h3>
          <ul>
            <li>About Us</li>
            <li>Whitepaper</li>
            <li>$N1 Token</li>
            <li>Directory</li>
          </ul>
        </div>
        <div class="list">
          <h3>RESOURCES</h3>
          <ul>
            <li>Help Center</li>
            <li>NFTify Branding</li>
            <li>Success Stories</li>
            <li>Video Tutorials</li>
            <li>Contact Support</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="lowerFooter">
      <div class="credits hide">
        <p>© Copyright NFTify Network. All Rights Reserved.</p>
      </div>
      <div class="socialMedia">
        <h3>The Leading No-code NFT Marketplace Solution</h3>
        <div class="icons">
          <div class="iconbutton">
            <img src="../assets/twittericon.svg" alt="" />
          </div>
          <div class="iconbutton">
            <img src="../assets/telegramicon.svg" alt="" />
          </div>
          <div class="iconbutton">
            <img src="../assets/facebookicon.svg" alt="" />
          </div>
          <div class="iconbutton">
            <img src="../assets/linkedinicon.svg" alt="" />
          </div>
          <div class="iconbutton">
            <img src="../assets/youtubeicon.svg" alt="" />
          </div>
          <div class="iconbutton">
            <img src="../assets/instagramicon.svg" alt="" />
          </div>
        </div>
      </div>
      <div class="credits">
        <p>Terms of Service Privacy Policy</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.footerContainer {
    padding-bottom:50px ;
  background: var(
    --d-9-d-9-d-9,
    linear-gradient(180deg, #52057b 0%, #000 100%)
  );

}
.upperFooter {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  padding-top: 34px;
  gap: 40px;
  padding-bottom: 50px;
}
.footerList {
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 104px;
  width: 50%;
}
ul {
  display: flex;
  flex-direction: column;
  list-style: none;
  gap: 28px;
}
li {
  color: var(--text-color, #d6d5a8);
  font-family: Poppins;
  font-size: 12px;
  font-style: normal;
  font-weight: 300;
  line-height: normal;
}
.list h3 {
  color: #fff;
  text-align: center;
  font-family: Poppins;
  font-size: 15px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  margin-bottom: 28px;
}
.list {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
}

.footerForm {
  display: flex;
  flex-direction: column;
  align-items: left;
  gap: 16px;
}

.footerForm h1 {
  color: #fff;
  font-family: Poppins;
  font-size: 28px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

.footerForm p {
  color: #fff;
  font-family: Poppins;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  width: 367px;
}

.emailSub {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.emailSub input {
  color: white;
  width: 272px;
  height: 30px;
  flex-shrink: 0;
  border-radius: 16px;
  opacity: 0.7;
  background: var(--background, #000);
  backdrop-filter: blur(10px);
  padding-left: 24px;
  outline: none;
  border: none;
}

.emailSub button {
  width: 111px;
  height: 30px;
  flex-shrink: 0;
  border-radius: 16px;
  background: var(--background, #000);
  backdrop-filter: blur(10px);
  color: #fff;
  font-family: Poppins;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  outline: none;
  border: none;
  cursor: pointer;
}

.createButton {
  color: #fff;
  font-family: Poppins;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  border-radius: 16px;
  background: var(--help-color, #52057b);
  backdrop-filter: blur(10px);
  width: 159px;
  height: 30px;
  flex-shrink: 0;
  outline: none;
  border: none;
  cursor: pointer;
}

.lowerFooter {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  justify-content: space-around;
  padding-top: 50px;
  border-top: 3px solid #816797;
}
.icons {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap:18px;
}
.iconbutton {
  border-radius: 16px;
  border: 1px solid #fff;
height: 50px;
width: 50px;
  flex-shrink: 0;
  opacity: .7;
    display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}
.socialMedia{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 16px; 
    width: 40%;
    }
.socialMedia h3{
    color: #FFF;
font-family: Poppins;
font-size: 20px;
font-style: normal;
font-weight: 500;
line-height: normal;
}
.credits{
    width: 30%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
 
    height: 100%;
}
.credits p{
    color: #FFF;
font-family: Poppins;
font-size: 12px;
font-style: normal;
font-weight: 400;
line-height: normal;
}
@media (max-width: 1024px) {
  .footerList {
    gap: 20px;
    flex-direction: column;
    width: 100%;
  }

  .footerList .list {
    width: 90%;
  }

  .footerForm {
    padding: 0 10px;
  }

  .footerForm h1 {
    font-size: 24px;
  }

  .footerForm p {
    font-size: 14px;
    max-width: 100%;
  }
  .list ul{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;

  }

  .emailSub {
    width: 100%;
    flex-direction: column;
    gap: 10px;
  }

  .emailSub input {
    width: 100%;
    padding: 0;
    text-align: center;
  }

  .emailSub button {
    width: 100%;
  }

  .createButton {
    width: 100%;
  }
  .lowerFooter 
  {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center  ;
    gap: 30px;
  }
  .hide{
    display:none;
  }
  .credits::after{
    content: "© Copyright NFTify Network. All Rights Reserved.";
        color: #FFF;
font-family: Poppins;
font-size: 12px;
font-style: normal;
font-weight: 400;
line-height: normal;
margin: 15px;
  }
}


@media (max-width: 768px) {
  .footerForm h1 {
    font-size: 20px;
  }

  .footerForm p {
    font-size: 12px;
  }

  .emailSub input {
    width: 100%;
    max-width: 100%;
  }

  .emailSub button {
    width: 100%;
  }

  .createButton {
    width: 100%;
  }
}
</style>
