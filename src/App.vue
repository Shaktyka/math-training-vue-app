<template>
  <div class="training">
    <h1>Math training</h1>
    <hr>
    <app-start-screen></app-start-screen>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Math'
    }
  }
};
</script>

<style scoped>
  .training {
    max-width: 700px;
    margin: 20px auto;
  }
</style>
