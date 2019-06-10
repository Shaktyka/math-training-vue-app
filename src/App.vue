<template>
  <div class="training">
    <h1>Math training</h1>
    <hr>
    <app-start-screen
      v-if="state == 'start'"
      @onStart="onStart"
    />
    <app-question v-else-if="state == 'question'" />
    <app-message v-else-if="state == 'message'" />
    <app-result-screen v-else-if="state == 'results'" />
    <!-- <div v-else>Unknown state</div> -->
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      state: 'start'
    }
  },
  methods: {
    onStart () {
      this.state = 'question';
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
