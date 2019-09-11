<template>
  <div class="house">
    House Details
    <h1>{{house.bedrooms}}</h1>
    <h1>{{house.bathrooms}}</h1>
    <h1>{{house.levels}}</h1>
    <h1>{{house.price}}</h1>
    <h1>{{house.year}}</h1>
    <h1>{{house.description}}</h1>
    <h1>{{house.imgUrl}}</h1>
  </div>
</template>


<script>
export default {
  name: "house",
  data() {
    return {};
  },
  mounted() {
    let payload = {
      houseId: this.$route.params.houseId
    };
    this.$store.dispatch("getHouseById", payload);
  },
  computed: {
    house() {
      return this.$store.state.activeHouse;
    }
  },
  methods: {},

  components: {}
};
</script>


<style scoped>
img {
  height: 400px;
}
</style>