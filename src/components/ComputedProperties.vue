<template>
  <h1>Computed Properties</h1>
  <h2>Full Name: {{fname}} {{lname}}</h2>
  <h2>full name using computed: {{fullName}}</h2>
  <button @click="changeFullName">Change Full Name</button>
  <button @click="items.push({id:4,title:'keyboard',price:50})">Add item</button>
  <h2>Total: {{total}}</h2>
  <template v-for="item in items" :key="item.id">
    <h2 v-if="item.price > 100">{{item.title}}: {{item.price}}</h2>
  </template>
  <!-- instead of writting above code you can use computed properties like in below code -->
    <h2 v-for="item in expensiveItems" :key="item.id">{{item.title}}: {{item.price}}</h2>
</template>

<script>
export default {
  data() {
    return{
      fname: 'rohit',
      lname: 'kuwar',
      items: [
        {
          id: 1,
          title: 'TV',
          price: 100
        },
        {
          id: 2,
          title: 'Mobile',
          price: 200
        },
        {
          id: 3,
          title: 'Laptop',
          price: 300
        }
      ]
    }
  },
  methods:{
    changeFullName(){
      this.fullName = 'guddu bhai'
    }
  },
  computed: {
    fullName:{
      get(){
        return `${this.fname} ${this.lname}`
      },
      set(value){
        const names = value.split(' ')
        this.fname = names[0]
        this.lname = names[1]
      }
    },
    total(){
      return this.items.reduce((total, elem) => (total = total + elem.price),0)
    },
    expensiveItems(){
      return this.items.filter(item => item.price > 100)
    }
  }
}
</script>