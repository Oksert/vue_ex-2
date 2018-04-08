<template>
  <div class="bar-container">
      <div class="bar-progress" :style="{width: progress*10 + '%'}">
          {{progress}}/10
      </div>
  </div>
</template>
<script>
export default {
    props: {
        progress: Number
    }
}
</script>
<style lang="scss" scoped>
    .bar {
        &-container{
            border: 1px solid black;
            border-radius: 2px;
            height: 40px;
        }
        &-progress {
            height: 100%;
            line-height: 40px;
            font-size: 25px;
            border-radius: 5px;
            box-shadow: 2px 0px 2px black;  
            background-color: aqua
        }
        
    }
</style>
