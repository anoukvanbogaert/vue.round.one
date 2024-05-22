<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div v-bind:id="myId">Hello my div: {{ myId }}</div>
    <button v-on:click="handleClick">Click</button>
    <h1 id="header">Header</h1>

    <form @submit.prevent="handleSubmit">
      <input type="text" />
      <button type="submit">Submit</button>
    </form>

    <button @click.once="OnBtnClick">Increase</button>
    <p>{{ number }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  methods: {
    handleClick() {
      const header = document.getElementById('header');
      header.style.color = 'red';
    },
    handleSubmit() {
      console.log('form submitted');
    },
    OnBtnClick() {
      this.number = this.number + 1;
    },
  },
  data() {
    return {
      myId: 'divId',
      number: 1,
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
