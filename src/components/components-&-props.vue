<template>
  <div>
    <h2>component & props</h2>

    <h2>hallo {{ name }}</h2>
    <h2>age {{ age }}</h2>
  </div>
</template>

<script>
export default {
  name: "ComponentsProps",
  //   props: ["name"],
  props: {
    name: {
      type: String,
      required: true,
      default: "aris",
    },
    age: Number,
  },
};
</script>

<style lang="scss" scoped></style>
