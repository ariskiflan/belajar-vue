<template>
  <div id="app">
    <!-- <VBind /> -->
    <!-- <VIf /> -->
    <!-- <listRenderingVue /> -->
    <!-- <Listkey /> -->
    <!-- <ConditionalListRendering /> -->
    <!-- <Methods /> -->
    <!-- <Eventhandling /> -->
    <!-- <FormHandling /> -->
    <!-- <Modifiers /> -->
    <!-- <ComputedProperty /> -->
    <!-- <Watchers /> -->
    <!-- <ComponentProps name="kiflan" :age="25" /> -->
    <!-- <h2>app component {{ name }}</h2>
    <ComponentA /> -->
    <!-- <button @click="showPopUp = true">open</button>
    <PopUp v-show="showPopUp" @close="popUpClose" /> -->

    <!-- <Slots /> -->

    <!-- <TemplateRefs /> -->

    <CompositionApi />
  </div>
</template>

<script>
// import VBind from "./components/v-bind.vue";
// import VIf from "./components/v-if.vue";
// import listRenderingVue from "./components/list-rendering.vue";
// import Listkey from "./components/list&key.vue";
// import ConditionalListRendering from "./components/conditional-list-rendering.vue";
// import Methods from "./components/methods.vue";
// import Eventhandling from "./components/event-handling.vue";
// import FormHandling from "./components/form-handling.vue";
// import Modifiers from "./components/modifiers.vue";
// import ComputedProperty from "./components/computed-property.vue";
// import Watchers from "./components/watchers.vue";
// import ComponentProps from "./components/components-&-props.vue";
// import ComponentA from "./components/component-a.vue";
// import PopUp from "./components/component-event-popup.vue";

// import Slots from "./components/slots.vue";

// import TemplateRefs from "./components/template-refs.vue";

import CompositionApi from "./components/composition-api.vue";

export default {
  components: {
    CompositionApi,
  },
  data() {
    return {
      // name: "aris kiflan",
      showPopUp: false,
    };
  },
  // provide() {
  //   return {
  //     username: this.name,
  //   };
  // },
  methods: {
    popUpClose(name) {
      this.showPopUp = false;
      console.log(name);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
