<template>
  <div class="content">
    <p>お客様リスト</p>
    <vue-good-table
            :columns="columns"
            :rows="rows"/>
  </div>
</template>
<script>
  export default {
    layout: 'menu',
    name: 'my-component',
    data(){
      return {
        columns: [
          {
            label: '氏名',
            field: 'name',
          },
          {
            label: '年齢',
            field: 'age',
            type: 'number',
          },
          {
            label: '登録日',
            field: 'createdAt',
            type: 'date',
            dateInputFormat: 'yyyy-MM-dd',
            dateOutputFormat: 'yyyy年 MM月 dd日',
          },
          {
            label: 'ご利用割合',
            field: 'score',
            type: 'percentage',
          },
        ],
        rows: [
          { id:1, name:"石川純平", age: 20, createdAt: '',score: 0.03343 },
          { id:2, name:"小手森泰介", age: 24, createdAt: '2011-10-31', score: 0.03343 },
          { id:3, name:"成田薫", age: 36, createdAt: '2011-10-30', score: 0.03343 },
          { id:4, name:"太田知孝", age: 55, createdAt: '2011-10-11', score: 0.03343 },
          { id:5, name:"中川純希", age: 40, createdAt: '2011-10-21', score: 0.03343 },
        ],
      };
    },
  };
</script>
<style>
  .content {
    padding: 20px;
    display: flex;
    flex-flow: column;
  }
</style>
