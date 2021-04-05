<template>
<h1>Hello Vue</h1>
<!-- <compo fname="rohit" lname="kuwar" />
<compo fname="swarup" lname="kendre" />
<compo fname="somesh" lname="itankar" />
<compo :fname="stack" :lname="role" /> -->
<!-- <prop-type id="myProp" title="My name is RK" :time='101' :isStart='true' /> -->
<!-- <button @click="showPopUp = true">Open</button>
<pop-up v-show="showPopUp" @close="showPopUp = false" /> -->
<!-- <Slots></Slots>
<Slots>this is slot</Slots>
<Slots><h1>this is h1 slot</h1></Slots>
<Slots><h2>this is h2 slot</h2></Slots>
<Slots><img src="https://picsum.photos/200" alt="random image"></Slots> -->
<NamedSlots>
  <template v-slot:header>
    <h3>Header</h3>
  </template>
  <template v-slot:content>
    <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis reiciendis rem ea ratione asperiores, obcaecati, voluptatem ut maxime tempora dolores quis dolorum deleniti expedita dignissimos minima quia quisquam, modi totam.</h3>
  </template>
  <template v-slot:footer>
    <h3>Footer</h3>
  </template>
</NamedSlots>
</template>

<script>
// import BindingInVue from './components/BindingInVue'
// import ListRendering from './components/ListRendering'
// import Method from './components/Method.vue'
// import EventHandling from './components/EventHandling.vue'
// import FormHandling from './components/FormHandling.vue'
// import ComputedProperties from './components/ComputedProperties.vue'
// import Compo from './components/Compo'
// import PropType from './components/PropType'
// import PopUp from './components/PopUp'
// import Slots from './components/Slots'
import NamedSlots from './components/NamedSlots'
export default {
  name: 'App',
  components: {
    NamedSlots
  },
  data() {
    return {
      stack: 'vue',
      role: 'developer',
      showPopUp: false
    }
  },
  provide: {
    username: 'rohit@123'
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
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
