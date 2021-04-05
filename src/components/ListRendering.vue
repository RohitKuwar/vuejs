<template>
  <h1>List Rendering</h1>
  <h2 v-for="(name, index) in names" :key="index">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.fname">{{ name.fname }} {{ name.lname }}</h2>
  <div v-for="actor in actors" :key="actor">
    <h3>{{actor.hero}}</h3>
    <h4 v-for="movie in actor.movies" :key="movie">{{movie}}</h4>
  </div>
  <h2 v-for="(name, key, index) in myInfo" :key="name">{{index}} {{key}}: {{name}}</h2>
  
  <template v-for="name in names" :key="name">
    <h2>{{name}}</h2>
    <hr>
  </template>

  <!-- conditional list rendering -->
  <template v-for="name in names" :key="name">
    <h2 v-if="name==='rohit'">{{name}}</h2>
  </template>

</template>

<script>
export default {
  data(){
    return{
      names: ['rohit', 'nikhil', 'chintan'],
      fullNames: [
        { fname: 'Swarup', lname: 'Kendre' },
        { fname: 'Ganesh', lname: 'Jatal' },
        { fname: 'Somesh', lname: 'Itankar' }
      ],
      actors: [
        {
          hero: 'Akshay Kumar',
          movies: ['Phir Hera Pheri', 'Welcome']
        },
        {
          hero: 'Rajkumar Rao',
          movies: ['Stree', 'Trapped']
        }
      ],
      myInfo: {
        fname: 'rohit',
        lanme: 'kuwar',
        age: 24
      }
    }
  }
}
</script>