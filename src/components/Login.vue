<template>
  <div class="login">
    <form @submit.prevent>
        <input v-model='name' placeholder='user name'/><br/>
        <input v-model='pass' placeholder='password'/><br/>
        <button type="submit" @click='handleSubmit'>ログイン</button>
    </form>
  </div>
</template>

<script>

export default {
  name: 'Login',
  data () {
    return {
      name: '',
      pass: ''
    }
  },
  methods: {
    handleSubmit: function () {
      console.log(this.name)
      // 本来はajax通信をする
      this.$router.push({ name: 'Home', params: { name: this.name } })
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
