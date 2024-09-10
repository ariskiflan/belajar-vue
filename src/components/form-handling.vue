<template>
  <div>
    <h2>form handling</h2>

    <div>
      <pre>
        {{ JSON.stringify(formValues, null, 2) }}
      </pre>
    </div>
    <div>
      <form @submit="SubmitForm">
        <div>
          <label for="name">name</label>
          <input type="text" id="name" v-model="formValues.name" />
        </div>

        <div>
          <label for="profile">Profile Summary</label>
          <textarea
            type="text"
            id="profile"
            v-model="formValues.profileSummary"
          />
        </div>

        <div>
          <label for="country">Country</label>
          <select id="country" v-model="formValues.country">
            <option value="">Select a Country</option>
            <option value="india">India</option>
            <option value="usa">USA</option>
            <option value="uk">UK</option>
          </select>
        </div>

        <div>
          <label for="job-location">Job Location</label>
          <select id="job-location" multiple v-model="formValues.jobLocation">
            <option value="india">India</option>
            <option value="usa">USA</option>
            <option value="uk">UK</option>
          </select>
        </div>

        <div>
          <input
            type="checkbox"
            id="remote"
            v-model="formValues.remoteWork"
            true-value="yes"
            false-value="no"
          />
          <label for="remote">Open to remote</label>
        </div>

        <div>
          <label for="">Skill Set</label>
          <input
            type="checkbox"
            id="html"
            value="html"
            v-model="formValues.skillSet"
          />
          <label for="html">html</label>
          <input
            type="checkbox"
            id="css"
            value="css"
            v-model="formValues.skillSet"
          />
          <label for="css">css</label>
          <input
            type="checkbox"
            id="jaavscript"
            value="javascript"
            v-model="formValues.skillSet"
          />
          <label for="jaavscript">javascript</label>
        </div>

        <div>
          <label for="">Years of experience</label>
          <input
            type="radio"
            id="0-2"
            value="0-2"
            v-model="formValues.yearsExperience"
          />
          <label for="0-2">0-2</label>
          <input
            type="radio"
            id="3-5"
            value="3-5"
            v-model="formValues.yearsExperience"
          />
          <label for="3-5">3-5</label>
          <input
            type="radio"
            id="6-10"
            value="6-10"
            v-model="formValues.yearsExperience"
          />
          <label for="6-10">6-10</label>
        </div>

        <div>
          <button>Submit</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "FormhandlingVue",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        remoteWork: "no",
        skillSet: [],
        yearsExperience: "",
      },
    };
  },
  methods: {
    SubmitForm(event) {
      event.preventDefault();
      console.log(this.formValues);
    },
  },
};
</script>

<style>
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
