<template>
  <div>
    <ComponentB />
  </div>
</template>

<script>
import ComponentB from "./component-b.vue";

export default {
  name: "componentsAProps",
  components: {
    ComponentB,
  },
};
</script>

<style lang="scss" scoped></style>
