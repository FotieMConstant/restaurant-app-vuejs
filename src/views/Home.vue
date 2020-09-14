<template>
  <div class="home">
    <v-row no-gutters>
      <v-col :cols="9">
        <v-card class="pa-2" tile outlined>
          <Map />
        </v-card>
      </v-col>

      <v-col :cols="3">
        <v-card class="pa-2" tile outlined>
          <h3 class="header">Nearby restaurants</h3>

          <div class="scrollable-content">
            <RestaurantList />
          </div>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src
import Map from "@/components/Map.vue";
import RestaurantList from "@/components/RestaurantList.vue";

export default {
  name: "Home",
  components: {
    Map,
    RestaurantList
  }
};
</script>

<style scoped>
.header {
  padding-top: 3px;
  padding-bottom: 9px;
}
.scrollable-content {
  width: 340px;
  overflow: scroll;
  overflow-x: hidden;
  margin-left: -5px;
}
</style>
