<template>
  <div>
    <h2>{{ 2 + 3 + 5 }}</h2>
    <h2>add methods - {{ add(2, 3, 5) }}</h2>
    <h2>add methods - {{ add(10, 5, 20) }}</h2>
    <h2>multiply methods - {{ multiply(10) }}</h2>

    <h2>count - {{ count }}</h2>

    <button @click="increment">increment</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  name: "methodsVue",
  setup() {
    const count = ref(0);

    function increment() {
      count.value++;
    }

    return {
      count,
    };
  },
  data() {
    return {
      baseMultiplier: 5,
    };
  },
  //   jangan gunakan arrow function untuk methods
  //   vue bind data object ke this keyword didalam methods
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
  },
};
</script>
