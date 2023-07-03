<script>

  import StarRating from './StarRating.vue'

  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    },
    components: {
    StarRating
    }
  }

</script>


<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>

  <StarRating />
</template>


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
