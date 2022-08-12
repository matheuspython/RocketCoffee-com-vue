<template>
  <TheHeade class="header" />
  <HeaderMobile />
  <TheMain />
  <MainResp />
</template>

<script>
import TheHeade from "./components/TheHeade.vue";
import TheMain from "./components/TheMain.vue";
import HeaderMobile from "./components/HeaderMobile.vue";
import MainResp from "./components/MainResp.vue";

export default {
  name: "App",
  components: {
    TheHeade,
    TheMain,
    HeaderMobile,
    MainResp
},
  methods: {
    
  },
};
</script>

<style>
:root {
  --backgrond: #000;
  --text-color: #FFF;
  --button: #8257E5;
  --border: #29292E;
  --border-menu-mobile: #A8A8B3;
  --text-color-menu-mobile: #E1E1E6;
    --secondary: #2f3136;
    --tertiary: rgb(32,34,37);
}
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html,
body {
  font-family: "Manrope", sans-serif;
}
::-webkit-scrollbar {
   width: 8px;
 }
 ::-webkit-scrollbar-thumb {
   background-color: var(--tertiary);
   border-radius: 4px;
 }
 ::-webkit-scrollbar-track {
   background-color: var(--secondary);
 }
body {
  background: var(--backgrond);
  overflow: hidden;

}
#app {
  width: 100%;
}
.container {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
}

@media screen and (max-width: 800px) {
  body{
    overflow: scroll;
    overflow-x:hidden ;
  }
  .blur{
    display: none;
  }
 
}
</style>
