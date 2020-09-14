<template>
  <v-app>
    <div class="container">
      <v-card v-for="Menu in menuStore" :key="Menu" class="mx-auto" max-width="344" id="menu">
        <v-list-item three-line>
          <v-list-item-content>
            <v-list-item-subtitle class="mb-n10">
              <strong>{{Menu.foodName}}</strong>
            </v-list-item-subtitle>
            <v-list-item-subtitle>
              <i>{{Menu.price}}</i>
            </v-list-item-subtitle>
          </v-list-item-content>

          <v-list-item-avatar tile size="100" color="grey">
            <v-img height="100%" v-bind:src="Menu.iconImage" />
          </v-list-item-avatar>
        </v-list-item>
        <v-card-actions class="justify-space-between">
          <div class="mx-2"></div>
          <v-btn @click="addToCard" class="more" color="secondary" fab x-small dark>
            <v-icon>mdi-plus</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </v-app>
</template>

<style scoped>
.container {
  text-align: left;
  height: 500px;
  padding-bottom: 30px;
}
.more {
  margin-top: -40px;
}
.menu {
  margin-top: 10px;
}
</style>

<script>
export default {
  data: () => ({
    menuStore: [
      {
        foodName: "Dambou, couscous aux épinards.",
        price: "3,000 FCFA",
        iconImage:
          "https://i.pinimg.com/736x/5e/ba/5f/5eba5f369aae5f912616a1ebcbe09716.jpg"
      },
      {
        foodName: "Foufou de banane",
        price: "400 FCFA",
        iconImage:
          "https://upload.wikimedia.org/wikipedia/commons/2/24/Foufou_banane_04.JPG"
      },
      {
        foodName: "Bonava ou ragoût d'agneau mauritanien.",
        price: "1,000 FCFA",
        iconImage:
          "https://djolo.net/wp-content/uploads/2015/01/MAURITANIE-BONAVA.jpg"
      },
      {
        foodName: "Beignets de poisson à l'ivoirienne.",
        price: "4,000 FCFA",
        iconImage:
          "https://myafricainfos.com/wp-content/uploads/2018/09/WhatsApp-Image-2018-09-21-at-18.08.00.jpg"
      },
      {
        foodName: "Injera, ou galette éthiopienne.",
        price: "800 FCFA",
        iconImage:
          "https://upload.wikimedia.org/wikipedia/commons/0/03/Alicha_1.jpg"
      },
      {
        foodName: "Couscous Méchoui Sénégalais.",
        price: "1,800 FCFA",
        iconImage:
          "https://img.cuisineaz.com/400x320/2016-04-28/i107816-couscous-mechoui-senegalais.jpg"
      },
      {
        foodName: "Couscous Méchoui Sénégalais.",
        price: "1,800 FCFA",
        iconImage:
          "https://img.cuisineaz.com/400x320/2016-04-28/i107816-couscous-mechoui-senegalais.jpg"
      }
    ],
    itemCount: 0
  }),
  methods: {
    addToCard() {
      //add code that you wish to happen on click
      alert("You are adding this to card!");
      this.itemCount += 1;
    }
  }
};
</script>