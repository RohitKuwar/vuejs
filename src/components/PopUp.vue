<template>
  <div>
    <h1>Pop Up component</h1>
    <h2>Custom Component Event</h2>
    <button @click="$emit('close')">Close</button>
  </div>
</template>

<script>
  export default {
    name: 'PopUp',
    emits: ['close']
  }
</script>

<style scoped>

</style>