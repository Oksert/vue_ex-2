<template>
    <div class="quote-editor">
        <h2>Quote</h2>
        <textarea name="" id="" cols="30" rows="10" v-model="currentQuote"></textarea>
        <button @click="addQuote()">Add Quote</button>
    </div>
  
</template>
<script>
export default {
    data: function () {
        return {
            currentQuote: ''
        }
    },
    methods: {
        addQuote() {
            this.$emit("addQuote", this.currentQuote)
            this.currentQuote = ''
        }
    }
}
</script>
<style lang="scss" scoped>
    button {
        display: block;
        margin: 10px auto;
    }
</style>
