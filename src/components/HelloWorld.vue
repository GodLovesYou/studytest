<template>
  <div class="container">
    <div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .container{
    width: 200px;
    height: 200px;
    margin: 50px;
    border: 1px solid;
    line-height: 200px;
    text-align: center;
    div{
      display: inline-block;
      width: 100px;
      height: 100px;
      margin-left: 200px;
      vertical-align: middle;
      border-radius: 20px;
      background: red;
    }
  }
</style>
