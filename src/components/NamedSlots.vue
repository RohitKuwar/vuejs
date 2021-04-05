<template>
  <div class="card">
    <div id="card-header">
      <slot name="header"></slot>
    </div>
    <div id="card-content">
      <slot name="content">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptatum nemo deserunt eum similique, nulla reprehenderit nam ipsam fugit assumenda accusamus.</slot>
    </div>
    <div id="card-footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'NamedSlots'
  }
</script>

<style scoped>

</style>