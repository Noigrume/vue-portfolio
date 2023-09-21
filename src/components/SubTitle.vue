<template>
  <div class="subtitle">
    <slot name="message"></slot>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
}
.subtitle {
  font-family: 'Mochiy Pop One', sans-serif;
  text-shadow: black 1px 1px 1px;
  color: yellow;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: #ffffff00;
  padding: 10px 0;
  text-align: center;
  z-index: 1000;
}
</style>
