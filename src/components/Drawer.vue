<script setup>
  import DrawerHead from './DrawerHead.vue'
  import CartListItem from './CartListItem.vue'
</script>

<template>
    <div class="fixed top-0 left-o h-full w-full bg-black z-10 opacity-70">
    </div>

    <div class="bg-white w-96 h-full fixed right-0 top-0 z-20 p-8">

        <DrawerHead />

        <CartListItem />

        <div class="flex flex-col gap-4 mt-7">
            <div class="flex gap-2">
                <span>Итого</span>
                <div class="flex-1 border-b border-dashed"></div>
                <b>95$</b>
            </div>

            <div class="flex gap-2">
                <span>Налог 12.5%</span>
                <div class="flex-1 border-b border-dashed"></div>
                <b>10$</b>
            </div>

            <button 
              disabled=""
              class="bg-lime-500 w-full mt-4 rounded-xl py-3 text-white hover:bg-lime-600 transition active:bg-lime-700 disabled:bg-slate-300 cursor-pointer">
              Оформить заказ
            </button>

        </div>

    </div>
</template>

