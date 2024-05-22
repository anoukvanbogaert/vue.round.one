<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div v-bind:id="myId">Hello my div: {{ myId }}</div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      myId: "divId",
    };
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#divId {
  background-color: red;
}
</style>
