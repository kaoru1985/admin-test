<template>
  <div class="content">
    <p>お客様リスト</p>
    <ul class="customer_list">
      <li>山田勝己</li>
      <li>山田勝己2</li>
      <li>山田勝己3</li>
    </ul>
  </div>
</template>
<script>
  export default {
    layout: 'menu'
  }
</script>

<style>
  .content {
    padding: 20px;
    display: flex;
    flex-flow: column;
  }
</style>
