<template>
  <div class="normalborder" style="width: 300px; padding: 10px">
    <h4>Deep</h4>

    <div class="normalborder">
      <h4>输入框</h4>
      <el-input class="myelinput margin10" placeholder="自定义高度">
        <i slot="prefix" class="el-input__icon el-icon-search"></i>
      </el-input>

      <el-input class="margin10" placeholder="原版">
        <i slot="prefix" class="el-input__icon el-icon-search"></i>
      </el-input>
    </div>

    <div class="normalborder">
      <h4>日期选择框</h4>
      <input placeholder="placeholder" />
      <div class="defualtmargin">
        <el-date-picker class="myelinputdate" type="date" placeholder="自定义">
        </el-date-picker>
      </div>
      <div class="defualtmargin">
        <el-date-picker type="date" placeholder="默认"> </el-date-picker>
      </div>
    </div>

    <div class="normalborder">
      <h4>下拉选择框</h4>
      <el-dropdown class="margin10 myeldrop" trigger="click">
        <span class="el-dropdown-link">
          自定义下拉菜单<i class="el-icon-arrow-down el-icon--right"></i>
        </span>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>黄金糕</el-dropdown-item>
          <el-dropdown-item>狮子头</el-dropdown-item>
          <el-dropdown-item>螺蛳粉</el-dropdown-item>
          <el-dropdown-item disabled>双皮奶</el-dropdown-item>
          <el-dropdown-item divided>蚵仔煎</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <br />
      <el-select v-model="value" placeholder="请选择">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        >
        </el-option>
      </el-select>
    </div>
  </div>
</template>

<script>
export default {
  data() {
      return {
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value: ''
      }
    }
};
</script>

<style  scoped lang="scss">
.myelinput {
  $myheight: 30px;
  width: 200px !important;
  height: $myheight !important;
  ::v-deep * {
    height: $myheight !important;
    line-height: $myheight !important;
    font-size: $myheight * 0.4;
  }
}

.myelinputdate {
  $myheight: 40px;
  width: 200px !important;
  height: $myheight !important;

  ::v-deep * {
    height: $myheight !important;
    line-height: $myheight !important;
    font-size: $myheight * 0.4;
    // color: black;
  }

  ::v-deep .el-input__inner {
    &::placeholder {
      color: black;
      // font-size: 16px;
    }
  }
}

.margin10 {
  margin: 10px;
}

.el-dropdown-menu {
  padding: 0px !important;
}

.el-dropdown-menu__item {
  padding: 0 8px !important;
}
</style>

<style >
/* 修改普通placeholder样式 */
/* https://blog.csdn.net/weixin_62277266/article/details/126663156 */
::-webkit-input-placeholder {
  /* WebKit, Blink, Edge */
  color: red;
}
</style>