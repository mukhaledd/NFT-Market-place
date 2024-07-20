<template>
  <div class="outterContainer">
    <div class="navContainer">
      <div class="navLeft">
        <img src="../assets/logo.svg" alt="logo" /> 
              <button class="navToggle" @click="toggleMenu" v-if="screenWidth<=1024">☰</button>
      </div>
      <div class="navRight" v-if="isMenuOpen">
 
        <div class="navTabs" >
          <ul>
            <li><router-link :to="`/`" class="router">Home</router-link></li>
            <li>About</li>
            <li><router-link :to="`/Blogs`" class="router">Blog</router-link></li>
            <li>Cart</li>
            <!-- <li> {{screenWidth}} </li> -->
          </ul>
        </div>
        <div class="navButtons">
          <button class="login" @click="checkScreenWidth">login</button>
          <button class="Signup">Sign Up</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data(){
    return{
     isMenuVisible:false,
     screenWidthMessage: '',
     width: window.innerWidth,
     screenWidth: window.innerWidth ,
     isMenuOpen: window.innerWidth > 1024
    }
  },
   methods:{
  
toggleMenu(){
  this.isMenuOpen=!this.isMenuOpen
},
 updateScreenWidth() {
      this.screenWidth = window.innerWidth;
         if(this.screenWidth>=1024){
          this.isMenuOpen=true
       }
 
    },

  },
        mounted() {
    
    window.addEventListener('resize', this.updateScreenWidth);
    
  },
  beforeDestroy() {

    window.removeEventListener('resize', this.updateScreenWidth);
  }
};
</script>

<style>
.navLeft{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding-top:20px ;
}
.navToggle{
  width:30px;
  height: 30px;
  
background-color:rgba(82, 5, 123, .5) ;
border: none;

  color: white;
  font-size: 16px;
  border-radius: 4px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.outterContainer {
    position:fixed;
z-index: 100;
  width: 100%;
  background: rgba(0, 0, 0, 0.25);
  backdrop-filter: blur(2px);
  display: flex;
}

.navContainer {
  width: 90vw;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 0 auto;
}
.navRight {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 85px;
}
.navTabs{
      display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}
.navTabs ul {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  text-decoration: none;
  list-style: none;
  gap: 45px;
}
li , .router {
  color: #fff;
  font-family: Poppins;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  text-decoration: none;
}

.login {
  width: 84px;
  height: 37px;
  flex-shrink: 0;
  border-radius: 16px;
  border: 1px solid var(--help-color, #52057b);
  color: #FFF;
  background-color: transparent;
font-family: Poppins;
font-size: 20px;
font-style: normal;
font-weight: 500;
line-height: normal;
outline: none;
cursor: pointer;
}

.Signup {
  width: 98px;
  height: 37px;
  flex-shrink: 0;
  border-radius: 16px;

  background: var(--help-color, rgba(82, 5, 123, .5));
  color: #FFF;
font-family: Poppins;
font-size: 20px;
font-style: normal;
font-weight: 500;
line-height: normal;
border: none;
outline: none;
cursor: pointer;
}
.navButtons{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 50px;
}

@media (max-width: 1024px) {
  .navContainer {
    flex-direction: column;
    align-items: center;
    margin-bottom:20px ;
  }

  .navRight {
    flex-direction: column;
    gap: 20px;
  }

  .navTabs ul {
    flex-direction: column;
    gap: 20px;
  }

  .navButtons {
    flex-direction: column;
    gap: 20px;
  }
}

@media (max-width: 768px) {
  .navContainer {
    width: 100%;
    padding: 0 20px;
  }

  .navTabs ul {
    gap: 15px;
  }

  .login,
  .signup {
    width: 100%;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .navTabs ul {
    gap: 10px;
  }

  .login,
  .signup {
    font-size: 18px;
  }
}
</style>
