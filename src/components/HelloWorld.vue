<template>
  <h1>{{ msg }}</h1>

  <Button>vant Button</Button>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
import { Button } from 'vant'

export default defineComponent({
  name: 'HelloWorld',
  components: {
    Button
  },
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  setup: () => {
    const count = ref(0)
    const useScriptSetup = ref(false);
    const useTsPlugin = ref(false);
    return { count, useScriptSetup, useTsPlugin }
  }
})
</script>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
