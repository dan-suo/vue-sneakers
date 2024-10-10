<script setup>
  import Drawer from './components/Drawer.vue';
  import Header from './components/Header.vue';
  import CardList from './components/CardList.vue';
</script>

<template>

  <!-- <Drawer /> -->

  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-10">

    <Header />

    <div class="p-7">

      <div class="flex justify-between items-center">

        <h2 class="text-3xl font-bold">Все кроссовки</h2>

        <div class="flex gap-4">
        <select class="py-2 px-3 border rounded-md outline-none">
          <option>По названию</option>
          <option>По цене (от самых дешевых)</option>
          <option>По цене (от самых дорогих)</option>
        </select>

        <div class="relative">
          <img 
            src="/search.svg" 
            alt="Search"
            class="absolute left-4 top-3"
          />
          <input 
            class="border rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
            type="text"
            placeholder="Поиск..." />
        </div>
        </div>  

      </div>

      <CardList />

    </div>

  </div>
  
</template>

<style scoped>

</style>
