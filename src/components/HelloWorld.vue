<template>
  <div>
    <div class="hello">
      <h1>{{ msg }}</h1>
    </div>
    <button @click="showUsername = !showUsername">Toggle Username</button>
    <div v-if="showUsername">
      <BigYellowUsername username="Nico" />
    </div>
  </div>
</template>

<script>
// import BigYellowUsername from './BigYellowUsername.vue'
export default {
  data () {
    return {
      showUsername: false
    }
  },
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    BigYellowUsername: () => import(/* webpackChunkName: "BigYellowUsername" */'./BigYellowUsername')
    // because we conditionaly render the username, we can prefetch the component and load when needed
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
