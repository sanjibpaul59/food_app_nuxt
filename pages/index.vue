<template>
  <v-container>
    <app-header />
    <div class="pa-4">
      <restaurantInfo :dataSource="fooddata" />
    </div>
  </v-container>
</template>

<script>
import { mapState } from "vuex";
import AppHeader from "../components/AppHeader.vue";
export default {
  components: { AppHeader },
  computed:{
    ...mapState(["fooddata"]),
  }
};
</script>

<style lang="scss" scoped>
</style>