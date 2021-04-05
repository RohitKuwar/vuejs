<template>
<div>
  <pre>
    {{ JSON.stringify(formValues, null, 2) }}
  </pre>
</div>
  <h1>Form Handling</h1>
  <form @submit="submitForm">
    <div>
    <label for="name">Name</label>
    <input type="text" id="name" v-model.trim="formValues.name">
    </div>
    <br>
    <div>
    <label for="age">Age</label>
    <input type="number" id="age" v-model.number="formValues.age">
    </div>
    <br>
    <div>
      <label for="message">Message</label>
      <textarea id="message" v-model="formValues.message"/>
    </div>
    <br>
    <div>
      <label for="country">Country</label>
      <select name="" id="country" v-model="formValues.country">
        <option value="india">India</option>
        <option value="usa">USA</option>
        <option value="australia">Australia</option>
      </select>
    </div>
    <br>
    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork">
      <label for="remoteWork">Open to remote work?</label>
    </div>
    <br>
    <div>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet">
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet">
      <label for="css">CSS</label>
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
      <label for="javascript">JavaScript</label>
    </div>
    <br>
    <div>
      <label>Gender:</label>
      <input type="radio" value="male" id="male" v-model="formValues.gender">
      <label for="">Male</label>
      <input type="radio" value="female" id="female" v-model="formValues.gender">
      <label for="">Female</label>
    </div>
    <br>
    <div>
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  data(){
    return{
      formValues: {
        name: '',
        age: null,
        message: '',
        country: '',
        remoteWork: false,
        skillSet: [],
        gender: ''
      }
    }
  },
  methods: {
    submitForm(event){
      event.preventDefault()
      console.log(this.formValues)
    }
  }
}
</script>

<style scoped>
label{
  padding: 1em;
}
input{
  padding: .1em;
}
</style>