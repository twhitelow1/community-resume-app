<template>
  <div class="home">
    <br>
    <h1>{{ message }}</h1>
  </div>
</template>

<style>
h1 {
  color: black;
}
</style>

<script>
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
    };
  },
  created: function () {},
  methods: {},
};
</script>