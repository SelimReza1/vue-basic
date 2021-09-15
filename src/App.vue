<template>
  <div>
    <pre>
      {{JSON.stringify(formValues, null, 2)}}
    </pre>
  </div>
<form @submit.prevent="submitForm">
  <div>
    <label for="name">Name</label>
    <input type="text" id="name" v-model.trim.lazy="formValues.name">
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
  <div>
    <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
    <label for="remoteWork">Open to Remote Work?</label>
  </div>
  <div>
    <input type="checkbox" id="css"  value="css" v-model="formValues.skillSet">
    <label for="remoteWork">CSS</label>
    <input type="checkbox" id="html"  value="html" v-model="formValues.skillSet">
    <label for="html">HTML</label>
    <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
    <label for="javascript">JAVASCRIPT</label>
  </div>
  <div>
    <label>Years Of Experience</label>
    <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
    <label for="0-2">0-2</label>
    <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
    <label for="3-5">3-5</label>
    <input type="radio" id="4-6" value="4-6" v-model="formValues.yearsOfExperience">
    <label for="4-6">4-6</label>
  </div>
  <div>
    <label for="age">Age</label>
    <input @keyup.enter="submitForm" type="number" id="age" v-model.number="formValues.age">
  </div>
<!--  <div>-->
<!--    <button>Submit</button>-->
<!--  </div>-->
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
      remoteWork: 'no',
      skillSet: [],
      yearsOfExperience: '',
      age: null,
    }
    }
  },
  methods: {
    submitForm(){
      console.log('Form Values', this.formValues)
    }
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
