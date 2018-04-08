<template>
  <div>
      <app-item :key="item" :delete-quote="deleteQuote" v-for="(item, index) in items" :msg=item :idx=index></app-item>
  </div>
</template>
<script>
import Item from './QuoteItem'
export default {
  components: {
      'app-item': Item
  },
  props: {
      items: Array,
      deleteQuote: Function
  }
}
</script>
<style lang="scss" scoped>
    div {
        margin-top: 25px;
    }
</style>

