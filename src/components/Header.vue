<template>
  <div class="header">
      <h1>Quotes</h1>
      <app-bar :progress="qNum"></app-bar>
  </div>
</template>
<script>
import Bar from './ProgressBar'
export default {
    components: {
        'app-bar': Bar
    },
    props: {
        qNum: {
            required: true
        }
    }
}
</script>
<style lang="scss" scoped>

</style>
