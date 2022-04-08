<template>
  <main v-if="!loading"></main>

  <main v-else class="flex flex-col align-center justify-center text-center">
    <div class="text-gray-500 text-3xl mt-10 mb-6">Fetching Data</div>
    <img
      :src="require('../assets/img/hourglass.gif')"
      alt=""
      class="w-24 m-auto"
    />
  </main>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
  data() {
    return {
      loading: true,
      title: "Global Statistics",
      date: "",
      stats: {},
      countries: [],
      loadingImg: require("../assets/img/hourglass.gif"),
    };
  },
  methods: {
    //   Fetch Covid Data
    async fetchCovidData() {
      const res = await fetch(
        "https://corona.lmao.ninja/v2/continents?yesterday=true&sort"
      );
      const data = res.json();
      return data;
    },
  },
  async created() {
    const data = this.fetchCovidData();
    console.log(data);

    this.loading = false;
  },
};
</script>
