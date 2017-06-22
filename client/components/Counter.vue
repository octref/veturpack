<template>
  <div class="counter-wrapper">
    <div class="counter">
      {{ count }}
    </div>
    <button @click="hello">Increment</button>
    <button @click="$store.commit('DECREMENT')">Decrement</button>
    <button @click="$store.dispatch('incrementAsync')">Increment Async</button>
  </div>
</template>

<script>
// @ts-check
export default {
  computed: {
    count () {
      return this.$store.state.count
    }
  },
  methods: {
    hello () {
      console.log('hello')
    }
  }
}
</script>

<style lang="scss">
.counter {
  margin: 100px auto;
  border-radius: 3px;
  width: 200px;
  height: 200px;
  text-align: center;
  line-height: 200px;
  font-size: 5rem;
  background-color: #f0f0f0;
  user-select: none;
}
</style>
