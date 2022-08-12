<template>
  <main>
    <BlurVue class="blur first"></BlurVue>
    <div class="text">
       <MessageSpace />
    </div>
    <img class="cafe" src="../assets/rocket-coffee.png" alt="">
    <BlurVue class="blur secund"></BlurVue>
  </main>
</template>

<script>
import MessageSpace from './MessageSpace.vue';
import BlurVue from './Blur.vue';
export default {
    components: { MessageSpace, BlurVue }
}
</script>

<style scoped>
    main{
        padding-top: 70px;
        color: var(--text-color);
        text-align: center;
    }
     
 
    .cafe{
        width: 100%;
        max-width: 600px;
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50%, 0px);
    }

    .first{
         top: -110px;
  right: -110px;
    }
    .secund{
        bottom: -110px;
        left: -110px;
    }
    @media screen and (max-width: 800px) {
        main{
            display: none;
        }
    }
</style>