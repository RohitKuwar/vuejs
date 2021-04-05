<template>
  <h1>Method</h1>
  <h2>{{add(2,3,5)}}</h2>
  <h2>{{multiply(5)}}</h2>
</template>

<script>
export default {
  data(){
    return{
      baseMultiplyer: 5
    }
  },
  methods: {
    add(a, b, c){
      return a + b + c
    },
    multiply(num){
      return num * this.baseMultiplyer
    }
  }
}
</script>