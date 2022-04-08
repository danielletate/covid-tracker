<template>
  <header>
    <div class="text-center bg-purple-700 text-white p-5 mb-10">
      <div class="text-3xl md:text-5xl font-bold mb-3">
        <img :src="require('../assets/img/bacteria.png')" class="h-10 w-10" />
        <h1>Covid-19 Tracker</h1>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>
