<template>
  <div>
    <NuxtWelcome />
  </div>
</template>

<script setup>
const { data: a } = await useFetch("/api/test");
const { data: b } = await useFetch("/api/test/123");
// a.value is [ 't', 'e', 's', 't' ] and typescript provide string[] type
console.log(a.value);
// b.value is test and typescript provide string[] type
console.log(b.value);
</script>
