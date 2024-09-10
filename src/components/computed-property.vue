<template>
  <div>
    <h1>Computed Property</h1>

    <p>{{ fullName }}</p>
    <button @click="changeFullName">Change FullName</button>

    <p>
      Total -
      {{ total }}
    </p>

    <template v-for="item in items" :key="item.id">
      <p v-if="item.price > 100">{{ item.name }} - {{ item.price }}</p>
    </template>

    <h2 v-for="item in expensiveItems" :key="item.id">
      {{ item.name }} {{ item.price }}
    </h2>
  </div>
</template>

<script>
export default {
  name: "ComputedPropertyVue",
  data() {
    return {
      firstName: "John",
      lastName: "Doe",
      items: [
        {
          id: 1,
          name: "item 1",
          price: 100,
        },
        {
          id: 2,
          name: "item 2",
          price: 200,
        },
        {
          id: 3,
          name: "item 3",
          price: 300,
        },
      ],
    };
  },

  methods: {
    changeFullName() {
      this.fullName = "Aris Kiflan";
    },
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`;
      },
      set(value) {
        const names = value.split(" ");
        this.firstName = names[0];
        this.lastName = names[1];
      },
    },
    total() {
      return (
        this.items.reduce((total, curr) => (total = total + curr.price)), 0
      );
    },
    expensiveItems() {
      return this.items.filter((item) => item.price > 100);
    },
  },
};
</script>

<style></style>
