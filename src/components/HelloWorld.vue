<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li v-for="num in list" :key="num">
        <span>{{num}} </span>
        <span>{{num * 2}} </span>
        <span>{{num * 3}} </span>
        <span>{{num * 4}} </span>
        <span>{{num * 5}} </span>
        <span>{{num * 6}} </span>
        <span>{{num * 7}} </span>
        <span>{{num * 8}} </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  computed: {
    list() {
      const result = [];
      for (var i = 0; i < 1785; i++) {
        result.push(i);
      }
      return result;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
