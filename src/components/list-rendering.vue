<template>
  <div>
    <!-- array of string -->
    <h2 v-for="(name, index) in names" :key="index">
      {{ index + 1 }}. {{ name }}
    </h2>

    <!-- array of object -->
    <h2 v-for="name in fullnames" :key="name.first">
      {{ name.first }} {{ name.last }}
    </h2>

    <!-- array of array -->
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{ actor.name }}</h2>
      <h3 v-for="movie in actor.movie" :key="movie">{{ movie }}</h3>
    </div>

    <!-- object -->
    <h2 v-for="(value, key, index) in myInfo" :key="index">
      {{ index + 1 }} {{ key }} : {{ value }}
    </h2>

    <template v-for="name in names" :key="name">
      <h2>{{ name }}</h2>
      <hr />
    </template>
  </div>
</template>

<script>
export default {
  name: "listRendering",
  data() {
    return {
      names: [" aris", "kiflan", "makarim"],
      fullnames: [
        { first: "aris", last: "kiflan" },
        { first: "bruce", last: "wayne" },
        { first: "clark", last: "kent" },
      ],
      actors: [
        {
          name: "christian bale",
          movie: ["batman", "the dark knight", "the dark knight rises"],
        },
        {
          name: "leonardo di caprio",
          movie: ["inception", "titanic", "the wolf of wall street"],
        },
      ],
      myInfo: {
        name: "aris kiflan",
        age: 20,
      },
    };
  },
};
</script>

<style></style>
