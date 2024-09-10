<template>
  <div>
    <h2>slots</h2>

    <Card></Card>
    <Card> Card Content </Card>
    <Card> <h2>Card Contents</h2> </Card>
    <Card> <img src="https://picsum.photos/200" alt="" /> </Card>

    <Card>
      <template v-slot:header>
        <h2>header</h2>
      </template>
      <template v-slot:footer>
        <h2>footer</h2>
      </template>
    </Card>
  </div>
</template>

<script>
import Card from "./card.vue";

export default {
  name: "SlotsVue",
  components: {
    Card,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
