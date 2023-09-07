<template>
  <!-- Home search bar -->
  <div
    class="font-serif w-full text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto z-40"
  >
    <input
      type="text"
      class="py-3 px-5 w-full text-2xl rounded-full focus:outline-none"
      :class="{ 'border border-red-500': cityError }"
      placeholder="Search by city..."
      v-model="city"
    />
    <button class="bg-sky-500 px-10 text-white" @click="handleSearch">
      Search
    </button>
  </div>
  <!-- /Home search bar -->
</template>
<script setup>
const city = ref("");
const cityError = ref(false);

const handleSearch = () => {
  if (!city.value) {
    cityError.value = true;
    return;
  }
  navigateTo(`/city/${city.value}/car`);
};
</script>
