<template>
  <div id="app">
    <app-header :q-num="quotes.length"></app-header>
    <app-quote @addQuote="addQuote($event)"></app-quote>
    <app-list :items=quotes :delete-quote="deleteQuote"></app-list>
  </div>
</template>

<script>
import Bar from './components/ProgressBar'
import Header from './components/Header'
import QuoteEditor from './components/QuoteEditor'
import QuoteList from './components/QuoteList'
export default {
  name: 'App',
  components: {
    'app-header': Header,
    'app-quote': QuoteEditor,
    'app-list': QuoteList,
  },
  data: function () {
    return {
      quotes: []
    }
  },
  methods: {
    addQuote($event) {
      if ($event)
     this.quotes.push($event)
    },
    deleteQuote(idx) {
      this.quotes.splice(idx,1)
    }
  }
}
</script>
<style lang="scss" scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  app-list {
    margin-top:45px;
  }
 
}
</style>
