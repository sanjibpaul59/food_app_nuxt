<template>
  <div>
    <section class="restaurantInfo">
      <div v-for="store in dataSource" :key="store.id">
        <h2>{{ store.name }}</h2>
        <p>Delivery time {{ store.deliveryTime }}</p>
        <p>Rating {{ store.rating }}</p>
        <p v-if="store.freeDelivery" class="label">
          <span>Free Delivery</span>
        </p>
        <v-row>
          <v-col
            cols="12"
            sm="12"
            md="4"
            lg="3"
            v-for="mitem in store.menu"
            :key="mitem.id"
          >
            <v-card elevation="4">
              <v-img height="240" :src="mitem.img"></v-img>
            </v-card>
            <v-card-title primary-title>
              {{ mitem.item }}
            </v-card-title>
            <v-card-text>
              <div class="my-1 subtitle-1">{{ mitem.price }}</div>
            </v-card-text>
            <v-card-actions>
              <nuxt-link :to="`/items/${mitem.id}`">
              <v-btn color="deep-purple lighten-2" text> View Item </v-btn>
              </nuxt-link>
              <v-btn color="deep-purple lighten-2" text> Add to Cart </v-btn>
            </v-card-actions>
          </v-col>
        </v-row>
      </div>
    </section>
  </div>
</template>

<script>

export default {
  props: {
    dataSource: {
      type: [Array, Object],
    },
  },
  data: () => ({
    loading: false,
    selection: 1,
  }),

  methods: {
    reserve() {
      this.loading = true;
      setTimeout(() => (this.loading = false), 2000);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>