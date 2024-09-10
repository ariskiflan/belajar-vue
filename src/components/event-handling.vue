<template>
  <div>
    <h2>event handling</h2>
    <h2>{{ name }}</h2>
    <div>
      <!-- multiple event handlers -->
      <button @click="changeName($event), increment(1, $event)">
        change name
      </button>
    </div>

    <h2>{{ count }}</h2>
    <div>
      <!-- event object -->
      <button @click="increment(1, $event)">increment 1</button>
      <button @click="increment(5)">increment 5</button>
      <button @click="decrement(1)">decrement 1</button>
      <button @click="decrement(5)">decrement 5</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventhandlingVue",
  data() {
    return {
      name: "joker",
      count: 0,
    };
  },
  methods: {
    changeName(event) {
      this.name = "batman";
      console.log(event);
    },
    increment(num, event) {
      this.count += num;
      console.log(event);
    },
    decrement(num) {
      this.count -= num;
    },
  },
};
</script>
