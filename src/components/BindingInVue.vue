<template>
<h1>Binding in Vue</h1>
<!-- binding data -->
<h2 v-text="sport"></h2>
<div>Hello {{name}} <h1 v-html="nickname"></h1></div>
<!-- binding html data -->
<h1 v-html="profession"></h1>
<!-- binding attributes -->
<h3 v-bind:id="headingId">Heading</h3>
<button v-bind:disabled="isDisabled">Bind</button>
<!-- binding class attributes conditionally -->
<h2 v-bind:class="isSold ? 'yes' : 'no'">Conditional Styling</h2>
<h2 v-bind:class="['a', 'b', 'c']">Apply multiple classes with Array</h2>
<h2 v-bind:class="{
  yes: !isSold,
  c: isDisabled
}">Apply multiple classes with objects</h2>
<!-- binding styles -->
<h2 v-bind:style="{color: success}">Inline Style</h2>
<!-- binding multiple styles & reason behind writting font size in quotes is that it is not a single word or you can use camelCase -->
<h2 v-bind:style="{
  color: fail,
  fontSize: headerSize + 'em',
  padding: paddingSize
  }">Inline Style</h2>
  <h2 v-bind:style="styleObject">Inline Style</h2>
  <h2 v-bind:style="[baseStyleObject, successStyleObject]">Inline Style</h2>
</template>

<script>
export default {
  name: 'BindingInVue',
  data(){
    return{
      name: 'Rohit',
      sport: "Cricket",
      nickname: 'Guddu',
      profession: "<h5>Developer</h5>",
      headingId: 'heading',
      isDisabled: true,
      isSold: false,
      success: 'greenyellow',
      fail: 'red',
      headerSize: .9,
      paddingSize: '.2em',
      styleObject: {
        color: 'white',
        backgroundColor: 'brown',
        border: '.1em solid yellow'
      },
      successStyleObject: {
        color: 'white',
        backgroundColor: 'green'
      },
      baseStyleObject: {
        fontSize: '1.5em',
        padding: '.5em'
      }
    }
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
.yes{
  color: green;
}
.no{
  color: red;
}
.a{
  color: blue;
}
.b{
  text-align: left;
}
.c{
  font-style: italic;
}
</style>
