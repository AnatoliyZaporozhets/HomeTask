<template>
  <div class="container">
    <table>
        <tr>
            <td>Назва продукту</td>
            <td>{{productName}}</td>
        </tr>
        <tr>
            <td>Вартість</td>
            <td>{{price}}</td>
        </tr>
        <tr>
            <td>ПДВ</td>
            <td>{{pdv}}</td>
        </tr>
        <tr>
            <td>До оплати</td>
            <td>{{}}</td>
        </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',

  props: {
    productName: {
      type: String,
      required: true,
    },
    price: {
      type: Number,
      required: true,
    },
    pdv: {
      type: Number,
      default: 0.05, //Обов"язковий параметр
    },
  },
}
</script>

<style lang="css" scoped>
.container{
    border: 2px solid black;
}
</style>
