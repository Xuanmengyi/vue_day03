<template>
  <div>
  <table border="1" width="500">  
    <caption><b>欢迎光临vue开发的收银系统水果店</b></caption> 
    <tbody>
      <tr>
      <td>苹果10￥/斤，折扣&lt;8折&gt;</td>
      </tr>
        <tr>
        <td>请输入你要购买的斤数:<input type="text" v-model="num"></td>  
        </tr>
      <tr>
        <td><button @click="pay">结账买单</button></td>
        </tr>
      <tr>
        <td>结账单:总价:<span>{{totalPrice}}</span>元&nbsp;&nbsp;折后价:<span>{{afterSalePrice}}</span>元&nbsp;&nbsp;省了:<span>{{reducePrice}}</span>元</td>
      </tr>
    </tbody>
  </table>
</div>
</template>

<script>
export default {
data(){
  return{
    num:0,
    totalPrice:0,
    afterSalePrice:0,
    reducePrice:0
  }
},
methods:{
  pay(){
    this.totalPrice=this.num*10
    this.afterSalePrice=this.totalPrice*0.8
    this.reducePrice=this.totalPrice-this.afterSalePrice
    
  }
}
}
</script>

<style>
tbody tr td{
  text-align: center;
}
</style>