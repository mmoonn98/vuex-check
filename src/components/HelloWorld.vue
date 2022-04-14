<template>
  <div class="hello">
    <h3>{{listReverse}}</h3>
  </div>
</template>

<script>
import {mapGetters,mapMutations,mapActions} from 'vuex'

export default {
  name: 'HelloWorld',
  props: {
    ...mapGetters([
      'listReverse'
    ])
  },
  methods : {
    ...mapMutations([
      'addcount'
    ])
  },
  ...mapActions([
    'timecount'
  ])
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
