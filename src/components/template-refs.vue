<template>
  <div>
    <h2>template refs</h2>

    <input type="text" ref="inputRefs" />
  </div>
</template>

<script>
export default {
  name: "templateRefs",
  mounted() {
    this.$refs.inputRefs.focus();
  },
};
</script>

<style lang="scss" scoped></style>
