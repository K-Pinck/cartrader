<template>
  <!-- Car cards -->
  <div
    class="car-card shadow border w-full overflow-hidden mb-5 cursor-pointer h-[200px]"
    @click="navigateTo('/car/${car.name}-${car.id}')"
  >
    <div class="flex h-full">
      <img :src="car.url" alt="" class="w-[300px] h-full" />
      <div class="p-4 flex flex-col items-start">
        <div>
          <h1 class="text-2xl text-blue-700">{{ car.name }}</h1>
        </div>
        <p class="text-gray-700">
          {{ car.description }}
        </p>
        <h1 class="mt-auto text-xl">{{ car.price }}</h1>
      </div>
    </div>
  </div>
  <!-- /Car cards -->
</template>
<script setup>
const props = defineProps({
  car: {
    type: Object,
    required: true,
  },
});
</script>
