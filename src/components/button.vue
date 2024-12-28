<template>
  <div :class="{ darkMode: changeColor }">
    <div id="counter">
      <h1 class="text">counter</h1>
      <h1 class="number">{{ names }}</h1>
    </div>
    <div id="button">
      <div class="form-check form-switch form-check-reverse but">
        <input
          class="form-check-input"
          type="checkbox"
          id="flexSwitchCheckReverse"
          v-model="changeColor"
        />
        <label class="form-check-label text-black" for="flexSwitchCheckReverse">
          dark mode
        </label>
      </div>
      <button @click="increase" class="but">increase</button>
      <button @click="reset" class="but">reset</button>
      <button @click="decrease" class="but">decrease</button>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const names = ref(0);
    const changeColor = ref(false);

    function increase() {
      names.value = names.value + 1;
    }

    function reset() {
      names.value = 0;
    }

    function decrease() {
      names.value = names.value - 1;
    }

    return { increase, reset, decrease, changeColor, names };
  },
};
</script>

<style>
div {
  color: red;
}
.darkMode {
  background-color: black;
}
#counter {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: hsl(209, 61%, 16%);
}

#button {
  margin-top: 30px;
  display: flex;
  gap: 20px;
  justify-content: center;
  color: hsl(209, 61%, 16%);
}

.number {
  font-size: 55px;
  font-family: sans-serif;
}

.text {
  font-size: 55px;
  font-family: sans-serif;
}
</style>
