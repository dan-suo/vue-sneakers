<script setup>
  import Card from './Card.vue'
  
  defineProps({
    items: Array
  })
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
          v-for="item in items"
          :key="item.id"
          :title="item.title" 
          :image-url="item.imageUrl" 
          :price="item.price"
          :isAdded="false"
          :isFavorite="false"
          :onClickAdd="onClickAdd"
          :onClickFavorite="onClickFavorite"
        />

      </div>
</template>

<style scoped>

</style>