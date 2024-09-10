<template>
  <div>
    <h2>Composition API</h2>

    <h3>Options - {{ o_firstName }}</h3>

    <h3>Composition - {{ c_firstName }}</h3>

    <h3>Composition - {{ greet }}</h3>

    <h3>Reactive - {{ reactiveName }}</h3>
  </div>
</template>

<script>
import { ref, reactive } from "vue";

export default {
  name: "CompositionApi",
  setup() {
    const c_firstName = ref("joni");
    c_firstName.value = "kiflan";

    const greet = `hello ${c_firstName.value}`;

    const state = reactive({
      firstName: "asura",
    });

    const reactiveName = `hello ${state.firstName}`;

    return {
      c_firstName,
      greet,
      reactiveName,
      state,
    };
  },
  data() {
    return {
      o_firstName: "Aris",
    };
  },
};
</script>

<style lang="scss" scoped></style>
