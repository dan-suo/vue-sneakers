<script setup>
  import { ref } from 'vue';
  import { onMounted } from 'vue';
  import axios from 'axios';

  import Drawer from './components/Drawer.vue';
  import Header from './components/Header.vue';
  import CardList from './components/CardList.vue';
  
  const items = ref([]);
  
  onMounted(async ()=> {

    /* ВАРИАНТ ЧЕРЕЗ FETCH
    fetch('https://6707bc588e86a8d9e42cb4c8.mockapi.io/sneakers/v1/items')
    .then(res => res.json())
    .then(data => {
      console.log(data);
    })
    })*/

    // ВАРИАНТ СИНХРОННОГО ПОЛУЧЕНИЯ ДАННЫХ
    //axios.get('https://6707bc588e86a8d9e42cb4c8.mockapi.io/sneakers/v1/items').then(resp => console.log(data));
    //  });

    // ВАРИАНТ АСИНХРОННОГО ПОЛУЧЕНИЯ ДАННЫХ
    
    try {
      const { data } = await axios.get('https://6707bc588e86a8d9e42cb4c8.mockapi.io/sneakers/v1/items');
      items.value = data;
    } catch (error) {
      console.log(error);
    }

  });

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

      <div class="mt-10">
        <CardList :items="items"/>
      </div>

    </div>

  </div>
  
</template>

<style scoped>

</style>
