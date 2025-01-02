<template>
  <div>
    <Galeri :isHomePage="false" />
  </div>
</template>

<script setup>
useHead({
  title: "Galeri",
  meta: [
    {
      name: "description",
      content: "Galeri Page",
    },
  ],
});
</script>
