<template>
  <div>
    <div v-html="myContent"></div>
  </div>

  <div>
    <h1 v-show="isShowing">v-show example</h1>
    <button @click="isShowing = !isShowing">
      {{ isShwoing ? 'HIDE' : 'SHOW' }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'DirectivesVue',
  methods: {},
  data() {
    return {
      myContent: "<b style='color:red'>This is my content</b>",
      isShowing: true,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#divId {
  background-color: red;
}
</style>
