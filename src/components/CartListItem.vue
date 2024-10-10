<script setup>
  import CartItem from './CartItem.vue'

  const onClickAdd = () => {
    alert('Добавлено в корзину');
  }

  const onClickFavorite =() => {
    alert('Добавлено в избранные')
  }
</script>

<template>
   <div class="flex flex-col flex-1 gap-4">
     <CartItem />
     <CartItem />
     <CartItem />
     <CartItem />
   </div>
</template>

<style scoped>

</style>