<template>
  <div id="father">
    <div class="wow">
        WOW
        <div class="eye">eye</div>
      </div>
    <div class="son">
      HHHH
      <div class="wow.eye">WAOOOYEEE</div>
      <div class="wow">
        WOW
        <div class="eye">eye</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#father {
  .son {
    color: aqua;
    &.wow.eye {
        color: red;
      }
    
  }
    &.wow.eye {
        color: red;
      }
}
</style>