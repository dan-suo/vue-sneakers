<script setup>
  import Card from './Card.vue'

  const onClickAdd = () => {
    alert('Добавлено в корзину');
  }

  const onClickFavorite =() => {
    alert('Добавлено в избранные')
  }
</script>

<template>
    <div class="grid grid-cols-4 gap-5 mt-7">

        <Card 
        title="Мужские кроссовки Nike Blazer Mid Suede" 
        image-url="/sneakers/sneakers-1.jpg" 
        :price="95"
        :isAdded="false"
        :isFavorite="false"
        :onClickAdd="onClickAdd"
        :onClickFavorite="onClickFavorite"
        />

      </div>
</template>

<style scoped>

</style>