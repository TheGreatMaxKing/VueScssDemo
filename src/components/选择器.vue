<template>
  <div id="father">
    嵌套选择器
    <br />
    <a>HTTP:???</a>
    <div class="son">
      <button>按钮</button>
    </div>
    <div class="group1">
      <h2>群组选择器</h2>
      <h3>G1</h3>
    </div>
    <div class="group2">
      <h2>群组选择器</h2>
      <h3>G2</h3>
    </div>
    <div id="ancestor">
      祖先
      <div id="offspring">
        SON
        <div id="offspring">GrandSon</div>
      </div>
    </div>
    <div id="brotherFather">
      兄弟选择器
      <div id="brother">brother</div>
      <p>nextbrother1</p>
      <p>nextbrother2</p>
    </div>
    <div id="嵌套属性">嵌套属性</div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
// 有利必有弊，你需要特别注意群组选择器的规则嵌套生成的css。
// 虽然sass让你的样式表看上去很小，但实际生成的css却可能非常大，这会降低网站的速度。

#father {
  // 在父选择器之前添加选择器
  #app & {
    // height: 300px;
    // background: red;
  }

  width: 200px;
  margin-top: 20px;
  color: blue;
  border: 1px solid red;
  a {
    color: rgb(167, 29, 158);
    //父选择器伪类
    &:hover {
      color: red;
      font-size: 18px;
    }
  }
  .son {
    color: rgb(224, 124, 10);
    button {
      background: rgba(222, 9, 147, 0.244);
      &:active {
        background: rgba(222, 9, 147, 1);
      }
    }
  }
}

//群组选择器
.group1,
.group2 {
  border: 1px solid blue;
  h1,
  h2 {
    color: red;
  }
}


////无需使用父元素标识符

//后代选择器
#ancestor {
  border: 1px solid red;

  #offspring {
    color: green;
  }
}

//相邻兄弟选择器
#brotherFather {
  border: 2px solid red;
}
#brother {
  ~ p {
    color: red;
  }

  + p {
    border: 1px solid blue;
  }
}
//嵌套属性
#嵌套属性 {
  color: green;
  border: {
    style: solid;
    width: 10px;
    color: rgb(21, 225, 62);
    left-width:20px;
    right-width: 5px;
  }
}
</style>