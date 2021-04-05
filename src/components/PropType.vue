<template>
  <div>
    <h1>Vue PropType</h1>
    <h2 v-bind="$attrs">{{title}} @ {{time}}</h2>
    <h3>Start: {{isStart ? 'yes' : 'no'}}</h3>
    <lorem/>
  </div>
</template>

<script>
import Lorem from './Lorem.vue'
  export default {
  components: { Lorem },
    name: 'PropType',
    props: {
      title: {
        type: String,
        required: true,
        default: 'guddu bhai'
      },
      time: Number,
      isStart: Boolean
    },
    inheritAttrs: false
  }
</script>

<style scoped>

</style>