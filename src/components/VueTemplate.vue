<template>
  <div class="VueTemplate">
    VueTemplate
  </div>
</template>

<script lang="ts">
/*
 *@Description: 
 *@ClassAuthor: sunny
 *@Date: 2021-06-03 11:20:34
*/
import { Options, Vue, setup, prop, createDecorator, mixins } from 'vue-class-component';
console.log( Options, Vue, setup, prop, createDecorator, mixins)
@Options({
  props: {
    value: String
  },
  components:{ }
})
export default class VueTemplate extends mixins(Vue) {

  // 初始data
  value!: string
  name = 'VueTemplate'

  // computed 属性
  get fullName():string{
    return this.name;
  }
  
  setup():unknown{
    return {
      value:this.getName()
    }
  }
  // method 方法
  private getName():string{
    return this.name
  }
  private init(value?:any) {
    console.log("init" + value)
  }

  // 实例初始化之后 钩子函数
  beforeCreate():void {
    this.init()
  }
  // 实例已经创建完成
  created():void {
    this.init()
  }
  // 挂载开始之前
  beforeMount():void {
    this.init()
  }
  // 挂载元素之后
  mounted():void {
    this.init()
  }
  // 数据更新时
  beforeUpdate():void {
    this.init()
  }
  // 数据更新后 dom更新后
  updated():void {
    this.init()
  }
  // 实例销毁之前
  beforeDestroy():void {
    this.init()
  }
  // 实例销毁后调用
  destroyed():void {
    this.init()
  }
}
</script>
<style lang="scss">
</style>
<style scoped lang="scss">
#VueTemplate{
  border: none;
}
</style>
