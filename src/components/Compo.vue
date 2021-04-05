<template>
  <div>
    <h1>Hi {{fname}} {{lname}}</h1>
  </div>
</template>

<script>
  export default {
    name: 'Compo',
    props: ['fname', 'lname']
  }
</script>

<style scoped>

</style>