<template>
  <div>
    <h1>Modifiers</h1>

    <div>
      <pre>
        {{ JSON.stringify(formValues, null, 2) }}
      </pre>
    </div>

    <form @submit.prevent="SubmitForm">
      <div>
        <label for="name">name</label>
        <input type="text" id="name" v-model.trim.lazy="formValues.name" />
      </div>

      <div>
        <label for="age">Age</label>
        <input
          @keyup.enter="SubmitForm"
          type="number"
          id="age"
          v-model.number="formValues.age"
        />
      </div>

      <!-- <div>
        <button>Submit</button>
      </div> -->
    </form>
  </div>
</template>

<script>
export default {
  name: "ModifiersVue",
  data() {
    return {
      formValues: {
        name: "",
        age: null,
      },
    };
  },
  methods: {
    SubmitForm() {
      console.log(this.formValues);
    },
  },
};
</script>

<style></style>
