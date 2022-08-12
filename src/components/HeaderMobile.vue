<template>
  <header class="mobile">
    <div class="container">
      <img src="../assets/logo-mobile.svg" alt="logo da rocketseat" />
      <img v-if="!showHeader" @click="showMenu" class="btn" src="../assets/menu-buguer-open.svg" alt="menu mobile" />
      <img v-if="showHeader"  @click="showMenu" class="btn rotate" src="../assets/menu-buguer-close.svg" alt="menu mobile" />

    </div>
  </header>
  <nav class="nav" v-if="showHeader">
    <ul>
      <li class="active">
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#">Menu</a>
      </li>
      <li>
        <a href="#">Recompensas</a>
      </li>
      <li>
        <a href="#">Gift Cards</a>
      </li>
      <li>
        <a href="#">Lojas</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showHeader: false
    }
  },
  methods: {
    showMenu(){
      this.showHeader = !this.showHeader
    }
  },
};
</script>

<style scoped>
header {
  display: none;
}
@media screen and (max-width: 800px) {
  .mobile {
    margin-top: 30px;
    display: block;
    width: 100%;
    height: 58px;
    border-bottom: 1px solid var(--border);
  }
  img {
    cursor: pointer;
  }

  .container {
    height: 100%;
    width: 100%;
    max-width: 700px;
    padding: 0 2%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .nav{
    position: fixed;
    top:  88px ;
    height: calc(100vh - 88px);
    background: var(--backgrond);
    width: 100%;
    z-index: 999;
  }
   .nav li{
    height: 55px;
    width: 100%;
    display: flex;
    align-items: center;
    border-bottom: 1px solid var(--border);
    padding-left: 25px;
   }
  .nav a{
    color: gray;
    text-decoration: none;
    transition: .4s;
  }
   .nav a:hover{
    color: var(--text-color);
   }
   .active{
    border-left: 5px solid var(--button);
   }
   .active a{
    color: var(--text-color);
   }
   .rotate{
    transition: .4s;
   }
   .rotate:hover{
    transform: rotate(360deg);
   }
}
</style>
