<template>
  <div class="hello">
    变量
    <div class='son'>
      www
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
<style scoped lang="scss">
// 全局变量
$testcolor:rgb(12, 12, 215);
$commonborder:1px solid red;
.hello{
  $lenth:100px;
  $double_lenth:$lenth*1.5;
  color: $testcolor;
  border:1px solid $testcolor;
  width: $lenth;
  height: $double_lenth;
}
.son{
  border: $commonborder;
}
</style>
