<template>
  <div>
    <pre>
      {{JSON.stringify(formValues, null, 2)}}
    </pre>
  </div>
<form>
  <div>
    <label for="name">Name</label>
    <input type="text" id="name" v-model="formValues.name">
  </div>
  <div>
    <label for="profile">Profile Summary</label>
    <textarea id="profile" v-model="formValues.profileSummary" />
  </div>
  <div>
    <label for="country"></label>
    <select id="country" v-model="formValues.country">
      <option value="">Select a Country</option>
      <option value="Bangladesh">Bangladesh</option>
      <option value="India">India</option>
      <option value="Thailand">Thailand</option>
    </select>
  </div>
  <div>
    <label for="jobLocation"></label>
    <select id="jobLocation" multiple v-model="formValues.jobLocation">
      <option value="Dhaka">Dhaka</option>
      <option value="Sylhet">Sylhet</option>
      <option value="Khulna">Khulna</option>
    </select>
  </div>
</form>
</template>

<script>

export default {
  name: 'App',
  data() {
    return{
    formValues:{
      name: '',
      profileSummary: '',
      country: '',
      jobLocation: [],
    }
    }
  },
  methods: {

  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}
.soldout {
  color: red;
}
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
input[type='text'],
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
