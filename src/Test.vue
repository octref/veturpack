<template>
  <div>
    <child :foo="" :bar="1"></child>
  </div>
</template>

<script>
import * as _ from 'lodash'
import { defineComponent } from 'vue'

import Child from './Child.vue'

export default defineComponent({
  components: {
    Component,
    Child
  },
  props: ['foo', 'bar']
})
</script>
