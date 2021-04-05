<template>
  <h1>Conditional Rendering</h1>
  <h2 v-if="num===0">The number is Zero</h2>
  <!-- v-else must come after v-if otherwise it will not work -->
  <h2 v-else-if="num>0">The number is positive</h2>
  <h2 v-else-if="num<0">The number is negative</h2>
  <h2 v-else>Not a number</h2>

  <!-- here we are using template to avoid creating unnecessory div node -->
  <template v-if="display">
      <div>Somesh</div>
      <div>Swarup</div>
      <div>Ganesh</div>
  </template>
  
  <h2 v-show="showElement">Using v-show</h2>
</template>

<script>
export default {
  data(){
    return{
      num: 5,
      display: true,
      showElement: false
    }
  }
}
</script>