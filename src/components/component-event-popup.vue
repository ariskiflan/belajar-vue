<template>
  <div>
    <h2>popup</h2>
    <input type="text" v-model="name" />
    <button @click="$emit('close', name)">close</button>
  </div>
</template>

<script>
export default {
  name: "PopUp",
  //   emits: ["close"],
  emits: {
    close(name) {
      if (!name) {
        return false;
      } else {
        return true;
      }
    },
  },
  data() {
    return {
      name: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>
