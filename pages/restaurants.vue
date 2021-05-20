<template>
  <div class="restaurant">
    <h1 class="restaurantheading">Restaurants</h1>
    <div>
      <AppSelect @change="selectedRestaurant = $event" />
    </div>
    <div>
      <RestaurantInfo :dataSource="filteredRestaurants" />
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";
import AppSelect from "../components/AppSelect.vue";
import RestaurantInfo from "../components/RestaurantInfo.vue";
export default {
  components: { RestaurantInfo, AppSelect },
  data: () => ({
    selectedRestaurant: "",
  }),
  computed: {
    ...mapState(["fooddata"]),
    filteredRestaurants() {
      if (this.selectedRestaurant) {
        return this.fooddata.filter((el) => {
          let name = el.name.toLowerCase();
          return name.includes(this.selectedRestaurant);
        });
      } else {
        return this.fooddata;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
</style>