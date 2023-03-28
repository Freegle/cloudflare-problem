<template>
  <div>
    Test page with client-only component.
    <client-only>
      <at-ta :members="members">
        <textarea></textarea>
      </at-ta>
    </client-only>
  </div>
</template>
<script>
import { defineAsyncComponent } from 'vue'

export default {
  components: {
    AtTa: defineAsyncComponent(() => import('vue-at/dist/vue-at-textarea')),
  },
  data () {
    return {
      members: ['Roxie Miles', 'grace.carroll', '小浩']
    }
  }
}
</script>
