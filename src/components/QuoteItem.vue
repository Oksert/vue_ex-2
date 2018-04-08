<template>
  <div class="cont"  @click="deleteQuote(idx)">
      {{msg}}
  </div>
</template>
<script>
export default {
  props: {
      msg: String,
      required: true,
      deleteQuote: Function,
      idx: Number
  }
}
</script>
<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Shadows+Into+Light');
    .cont {
        max-width: 300px;
        max-height: 100px;
        overflow: hidden;
        font-family: 'Shadows Into Light', cursive;
        font-size: 40px;
        padding: 10px 20px;
        font-weight: bold;
        border: 1px solid gray;
        border-radius: 5px;
        box-shadow: 0px 0px 3px 2px gray;
        margin: 15px;
        display: inline-block;
        &:hover {
            background-color: red;
        }
    }
</style>
