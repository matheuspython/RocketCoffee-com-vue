<template>
  <header>
    <div class="container">
      <img src="../assets/logo-desktop.svg" alt="logo do site" />
    
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Menu</a></li>
        <li><a href="#">Recomponsas</a></li>
        <li><a href="#">Gift Cards</a></li>
        <li><a href="#">Lojas</a></li>
      </ul>
      <ButtonVue>PEGAR MEU CAFÉ</ButtonVue>
    </div>
  </header>
</template>

<script>
import ButtonVue from './ButtonVue.vue';
export default { components: { ButtonVue } };
</script>

<style scoped>
header{
    margin-top: 20px;
    width: 100%;
    text-align: center;
    display: flex;
    justify-content: center;
    align-content: center;
    align-items: center;
}

header .container{
  width: 100%;
  padding: 0 2%;
    display: flex;
    justify-content: space-between;
    align-items: center;

}
header .container ul {
    display: flex;
    gap: 9px;
    list-style-type: none;
    justify-content: center;
}
header a{
  color: #fff;
  font-size: 16px;
  text-decoration: none;
  font-family: Manrope;
     transition: all 0.4s ease 0s;
}
header a:hover, header:active{
  opacity: 0.7;
}
button{
    border: 1px solid var(--button);
    background: transparent;
    color: #fff;
    width: 172px;
    height: 37px;
    border-radius: 6px;
    cursor: pointer;
        transition: all 0.4s ease 0s;
}
  button:hover, button:focus{
      background-color: #8257e5;
    }
    @media screen and (max-width: 800px) {
      header{
         
    display: none;
  }
    
    }
</style>
