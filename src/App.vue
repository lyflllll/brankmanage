<template>
  <div id="app">
    <h1>品牌管理</h1>
    <table class="table table-bordered">
      <thead>
        <tr>
          <th>编号</th>
          <th>资产名称</th>
          <th>价格</th>
          <th>创建时间</th>
          <th>操作</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="txt in list" :key="txt.id">
          <td>{{txt.id}}</td>
          <td>{{txt.name}}</td>
          <td v-if="txt.price>100" :style="{color:'red'}">{{txt.price}}</td>
          <td v-else>{{txt.price}}</td>
          <td>{{txt.time}}</td>
          <td>{{del}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data(){
    return{
      list: [
        { id: 100, name: "外套", price: 199, time: new Date('2010-08-12')},
        { id: 101, name: "裤子", price: 34, time: new Date('2013-09-01') },
        { id: 102, name: "鞋", price: 25.4, time: new Date('2018-11-22') },
        { id: 103, name: "头发", price: 19900, time: new Date('2020-12-12') }
      ],
      del:'删除'
    }
  }
}
</script>

<style>

</style>