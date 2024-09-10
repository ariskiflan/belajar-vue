<template>
  <div>
    <h2>component B username {{ username }}</h2>
  </div>
</template>

<script>
export default {
  name: "componentsBProps",
  inject: ["username"],
};
</script>

<style lang="scss" scoped></style>
