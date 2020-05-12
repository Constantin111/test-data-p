<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <comp-one></comp-one>
    <comp-two></comp-two>
  </div>
</template>

<script>
import CompOne from './CompOne'
import CompTwo from "./CompTwo";
export default {
  name: 'HelloWorld',
    components: {CompTwo, CompOne},
    props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
