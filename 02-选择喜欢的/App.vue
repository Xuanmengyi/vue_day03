<template>
  <div>
    <div>请选择你喜欢的专栏</div>
    <span v-for="(item,index) in arr" :key="index"><input type="checkbox" v-model="hobby" :value="item">{{item}}</span>
    <ul>
      <li v-for="(item,index) in hobby" :key="index">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
data(){
  return{
    arr:["科幻", "喜剧", "动漫", "冒险", "科技", "军事", "娱乐", "奇闻"],
    hobby:[]
  }
}
}
</script>

<style>

</style>