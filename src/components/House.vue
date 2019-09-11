<template>
  <div class="house col-3 border rounded">
    <h5>{{houseProp.bedrooms}}</h5>
    <h5>{{houseProp.bathrooms}}</h5>
    <h5>{{houseProp.year}}</h5>
    <h5>{{houseProp.price}}</h5>
  </div>
</template>


<script>
export default {
  name: "house",
  house: ["houseProp"],
  data() {
    return {};
  },
  computed: {},
  methods: {
    viewHouse() {
      this.$router.push({
        name: "house",
        params: { houseId: this.houseProp._id }
      });
    }
  },
  components: {}
};
</script>


<style scoped>
</style>