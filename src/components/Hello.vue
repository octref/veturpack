<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul class="links">
      <li><a href="https://vuejs.org" target="_blank">Vue</a></li>
      <li><a href="https://github.com/vuejs/vetur" target="_blank">Vetur</a></li>
      <li><a href="https://code.visualstudio.com/" target="_blank">VSCode</a></li>
      <li><a href="https://github.com/octref/veturpack" target="_blank">Veturpack</a></li>
    </ul>
    <h2>Things to Try</h2>
    <ul class="tips">
      <li><button @click="hype()">H Y P E</button></li>
      <li>Open <span class="code">Hello.vue</span> and hover on <span class="code">this.msg</span></li>
      <li>Now hover on <span class="code">this</span></li>
      <li>Start typing another <span class="code">this</span> with a dot</li>
      <li>You have <span class="code">vue-router</span> as dependency right?</li>
      <li>So don't miss <span class="code">this.$router</span> with a dot </li>
      <li>Final Pro Tip: Put <span class="code">//@ts-check</span> on the top of your script block, and try stupid things like <span class="code">this.msg = 42</span></li>
      <li>You own <a href="https://github.com/octref">@octref</a> a <button @click="tweet">tweet</button></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Try Vue 2.5 new types in Vetur'
    }
  },
  computed: {
    encodedTweetUri () {
      const hypedTweet = this.msg + ' https://github.com/octref/veturpack/tree/new-types'
      return encodeURI(`https://twitter.com/intent/tweet?text=${hypedTweet}`)
    }
  },
  methods: {
    hype () {
      this.msg += '!'
    },
    tweet () {
      window.open(this.encodedTweetUri)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul { padding: 0; }
li { list-style-type: none; }
.code { color: #6f92ba; }

ul.links li {
  list-style-type: none;
  display: inline-block;
  margin: 0 16px;
}
ul.tips li {
  margin-bottom: 10px;
}

a {
  color: #42b983;
}

</style>
