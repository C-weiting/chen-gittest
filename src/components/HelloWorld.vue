<template>
  <div class="hello">
      <el-button @click="add">增加</el-button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  created () {
     this.init();
  },
  data () {
    return {
      msg: {
        name: 'chen'
      }
    }
  },
  methods: {
    init (){
      console.log(this.$store.state)
    },
    add () {
      this.$store.commit('increment')
      console.log(this.$store.state.count)
      this.$set(this.msg, 'age', 18);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
