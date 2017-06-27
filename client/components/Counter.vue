<template>
  <div class="counter-wrapper">
    <div class="counter">
      {{ count }}
    </div>
    <button @click="$store.commit('INCREMENT')">Increment</button>
    <button @click="$store.commit('DECREMENT')">Decrement</button>
    <button @click="$store.dispatch('incrementAsync')">Increment Async</button>
    <div>
      <img src="https://vuejs.org/images/logo.png" width="200" height="200" />
    </div>
  </div>
</template>

<script>
// @ts-check
import * as _ from 'lodash'

export default {
  computed: {
    count () {
      const a = _.add(1, 2);
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
