<template>
  <div>
    <h2 v-if="num === 0">The number is zero</h2>
    <h2 v-else-if="num < 0">the number is negative</h2>
    <h2 v-else-if="num > 0">the number is positive</h2>
    <h2 v-else>not a number</h2>

    <template v-if="display">
      <h2>aris</h2>
      <h2>kiflan</h2>
      <h2>makarim</h2>
    </template>

    <h2 v-show="showElement">v show element</h2>
  </div>
</template>

<script>
export default {
  name: "VIf",
  data() {
    return {
      num: 10,
      display: true,
      showElement: true,
    };
  },
};
</script>

<style></style>
