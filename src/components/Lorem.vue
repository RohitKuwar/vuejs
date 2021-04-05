<template>
  <div class="lorem">
    <h1>Lorem Component</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima ratione accusantium quidem voluptatibus! Provident, corporis aliquam iste magni, modi dignissimos earum optio, aperiam repudiandae necessitatibus doloribus commodi minus nostrum voluptatem illum unde. Accusantium eveniet pariatur ad molestias fugit nihil ipsam amet, autem nisi iste sed commodi maxime alias voluptates voluptas vero aspernatur rerum sit neque explicabo dolores temporibus nulla asperiores? Officia numquam molestiae amet repellat incidunt. Aspernatur in maiores repellat, earum sapiente et! Accusantium maiores porro doloremque, possimus quasi iusto, dolorem, eum cum magnam nam saepe ratione hic! Mollitia unde facere molestiae natus? Debitis dolore maiores corporis veritatis facere sed.
    </p>
    <ul>
      <li>Virat KOhli</li>
      <li>Sachin Tendulkar</li>
      <li>MS Dhoni</li>
      <li>Rohit Sharma</li>
      <li>Sureh Raina</li>
    </ul>
  </div>
  <hello-world/>
</template>

<script>
import HelloWorld from './HelloWorld.vue'
export default {
  components: { HelloWorld },
  name: 'Lorem',
}
</script>

<style scoped>
.lorem {
  color: green;
}

p {
  font-size: 1.3em;
}

ul li {
  list-style-type: none;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}
</style>