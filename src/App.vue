<template>
  <HeaderComponent />
  <div class="container">
    <HomeView />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent";
import HomeView from "./views/HomeView";

export default {
  name: "App",
  components: {
    HeaderComponent,
    HomeView,
  },
};
</script>
