<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>Let's Build an awesome app</p>    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
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
p {
  color: #kabir;
  font-size: 1rem;
}
</style>
