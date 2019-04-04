<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

import Counter from './Counter.vue'
import * as _ from 'lodash'

export default Vue.extend({
  components: {
    Counter
  }
})
</script>
