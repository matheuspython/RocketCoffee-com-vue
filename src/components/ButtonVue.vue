<template>
  <button type="button">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "ButtonVue",
};
</script>

<style scoped>
button {
  cursor: pointer;
  background: transparent;
  color: var(--text-color-menu-mobile);
  width: 174px;
  height: 35px;
  border-radius: 6px;
  border: 1px solid var(--button);
  padding: 10px, 30px, 10px, 30px;
  transition: all 0.4s ease 0s;
}
button:hover,
button:focus {
  background-color: #8257e5;
}
</style>
