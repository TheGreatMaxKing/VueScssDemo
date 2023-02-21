<template>
  <div style="border:1px solid red; margin-top:20px;width:200px">
    <h2>指令</h2>
    <div id="if" class="normalborder">IF</div>
    <div id="for">
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
$num: 2;
#if {
  @if $num == 1 {
    color: blue;
  } @else if $num == 2 {
    color: red;
  } @else {
    color: black;
  }
}

#for{
    @for $i from 1 through 2{
        li:nth-child(#{$i}){
            color: blue;
            height: $i*30px;
            border: 1px solid blue;
        }
    }
}
</style>