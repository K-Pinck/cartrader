<template>
  <div>
    <CarDetailsHero />
    <CarDetailsAttributes />
    <CarDetailsDescription />
    <CarDetailsContact />
  </div>
</template>

<script setup>
const route = useRoute();
const {toTitleCase} = useUtilities();

definePageMeta({
  layout: "custom",
});

useHead({
  title: toTitleCase(route.params.name),
});


</script>
