<template>
  <main>
    <div class="container">
        <div class="text-field">
          <h1>
            O café que fará seu 
            código decolar para 
            o próximo nível.
          </h1>
        <ButtonVue>PEGAR MEU CAFÉ <img src="../assets/arrow.svg" alt=""></ButtonVue>
       </div>
    </div>
  </main>
      <section class="coffe-message">
        <MessageSpace />

        <img class="cafe" src="../assets/rocket-coffee.png" alt="rocket coffe">
        <Blur class="blur" />
      </section>

</template>
<script>
import ButtonVue from './ButtonVue.vue';
import MessageSpace from './MessageSpace.vue';
import Blur from './Blur.vue';
export default { components: { ButtonVue, MessageSpace, Blur } };
</script>
<style scoped>
main {
  display: none;
}
.coffe-message{
  display: none;
}
@media screen and (max-width: 800px) {
  main {
    display: block;
    width: 100%;
    height: 100vh;
  color: #fff;

  }
  .container{
    width: 100%;
    justify-content: center;
    display: flex;
    flex-direction: column;
    height: 100%;
    align-items: center;
  }
  .text-field{
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 88px;
  }
  .text-field h1{
    width: 80%;
    margin: 0 auto;
    font-weight: 600;
    font-size: 40px;
    letter-spacing: 2%;
    text-align: center;
  }
  .text-field button{
     display: flex;
     justify-content: space-around;
     align-items: center;
  }
  .coffe-message{
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #fff;
    text-align: center;
  }
  .cafe{
    width: 100%;
  }
 .blur{
    display: block;
    position: absolute;
    bottom: 0;
  }
}
 
</style>
