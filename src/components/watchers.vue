<template>
  <div>
    <h1>Watchers</h1>

    <h2>Volume Tracker (0-20)</h2>
    <h2>Current Volume {{ volume }}</h2>

    <div>
      <button @click="volume += 2">increment</button>
      <button @click="volume -= 2">decrement</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "WatchersVue",
  data() {
    return {
      volume: 0,
    };
  },
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert("volume is too high");
      }
    },
  },
};
</script>

<style></style>
