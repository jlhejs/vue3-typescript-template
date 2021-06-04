<template>
  <div class="HelloWorld">
    HelloWorld81
  </div>
</template>

<script lang="ts">
import { Options, Vue, setup, prop, createDecorator, mixins } from "vue-class-component";
@Options({
  props: {
    value: String
  },
  components:{}
})
export default class HelloWorld extends mixins(Vue) {
  // 初始data
  name = "HelloWorld"

  // computed 属性
  get fullName():string {
    return '';
  }

  setup():unknown {
    return {}
  }

  // method 方法
  private init(value:any="") {
    return {}
  }

  // 实例初始化之后 钩子函数
  beforeCreate():void {
    console.log("beforeCreate")
  }

  // 实例已经创建完成
  created():void {}

  // 挂载开始之前
  beforeMount():void {}

  // 挂载元素之后
  mounted():void {}

  // 数据更新时
  beforeUpdate():void {}

  // 数据更新后 dom更新后
  updated():void {}

  // 实例销毁之前
  beforeDestroy():void {}

  // 实例销毁后调用
  destroyed():void {}
}
</script>
<style lang="scss">
</style>
<style scoped lang="scss">
#HelloWorld{
  border: none;
}
</style>