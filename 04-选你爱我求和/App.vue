<template>
  <div>
    <span v-for="(item,index) in arr" :key="index"><input type="checkbox" :value="item" v-model="num">{{item}}</span>
    <div>你选中的元素，累加的值和为
      <span>{{sum}}</span>
    </div>
  </div>
</template>

<script>
export default {
data(){
  return{
    arr:[9, 15, 19, 25, 29, 31, 48, 57, 62, 79, 87],
    num:[]
  }
},
computed:{
  sum(){
    return this.num.reduce((prev,next)=>prev+next,0)
  }
}
}
</script>

<style>

</style>