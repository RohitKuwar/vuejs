<template>
  <h1>Event Handling</h1>
  <h2>{{name}}</h2>
  <!-- <button v-on:click="name = 'guddu'">Change Name</button> -->
  <!-- instead of using v-on:click you can use shorthand '@' -->
  <button @click="changeName">Change Name</button>
  <h2>Count: {{count}}</h2>
  <button @click="increment">Increment</button>
  <button @click="decrement">Decrement</button>
</template>

<script>
export default {
  data(){
    return{
      name: 'rohit',
      count: 0
    }
  },
  methods:{
      increment() {
        return this.count += 1
      },
      decrement() {
        return this.count -= 1
      },
      changeName(){
        // if(this.name==='rohit'){
        //   return this.name == 'guddu'
        // }else{
        //   return this.name == 'rohit'
        // }
        this.name = 'guddu'
      }
    }
}
</script>