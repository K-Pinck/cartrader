<template>
  <div>
    <!-- Cars page -->

    <div class="mt-32 flex">
      <CarSidebar />
      <NuxtPage />
    </div>

    <!-- /Cars page -->
  </div>
</template>

<script setup>
const route = useRoute();
const { toTitleCase } = useUtilities();

definePageMeta({
  layout: "custom",
});

useHead({
  title: `${
    route.params.make ? toTitleCase(route.params.make) : "Cars"
  } in ${toTitleCase(route.params.city)}`,
});
</script>
