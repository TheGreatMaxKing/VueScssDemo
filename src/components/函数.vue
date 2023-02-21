<template>
  <div class="normalborder" style="width: 300px; padding: 10px">
    函数 自定义元素高度 随机颜色
    <div class="container">
      <div class="inner" v-for="index of 5" :key="index">
        {{ index }}
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
$grid-height: 40px;
$childnum: 5;

@function containerheight($n) {
  @return $grid-height * $n;
}

@function randomColor() {
  @return rgb(255 * random(), 255 * random(), 255 * random());
}

.container {
  height: containerheight($childnum);
  width: 200px;
  border: 10px solid orange;
  @for $i from 1 through $childnum {
    div:nth-child(#{$i}) {
      background: randomColor();
    }
  }
}

.inner {
  height: $grid-height;
  width: 100%;
  border: 1px solid rgb(241, 240, 240);
  box-sizing: border-box;
}
</style>