<template>
  <buttonCounter />
</template>

<script>
import button from "./components/button.vue";

export default {
  components: {
    buttonCounter: button,
  },
  setup() {},
};
</script>

<style>
#app {
  width: 100%;
  height: fit-content;
  display: flex;
  flex-direction: column;
  border: 1px solid red;
}
</style>
