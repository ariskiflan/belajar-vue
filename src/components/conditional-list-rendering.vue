<template>
  <div>
    <template v-for="name in names" :key="name">
      <h2 v-if="name === 'Bruce'">{{ name }}</h2>
    </template>
  </div>
</template>

<script>
export default {
  name: "conditionalListRendering",
  data() {
    return {
      names: ["Bruce", "Clark", "Diana", "Barry"],
    };
  },
};
</script>
