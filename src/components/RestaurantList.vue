<template>
  <div>
    <div id="RestaurantList" sm="4">
      <v-card
        class="mx-auto"
        max-width="350"
        v-for="Restaurant in Resto"
        :key="Restaurant"
        style="box-shadow: 0px 0px 5px gray;"
        id="card"
      >
        <v-img
          class="white--text align-end"
          height="150px"
          v-bind:src="Restaurant.coverImage"
          gradient="rgba(255,0,0,0.2), rgba(25,32,72,.7)"
        >
          <v-card-title id="title">{{Restaurant.name}}</v-card-title>
        </v-img>
        <v-card-subtitle class="pb-0">
          <i>{{Restaurant.address}}</i>
        </v-card-subtitle>
        <v-rating
          v-model="Restaurant.rating"
          color="yellow darken-3"
          background-color="Gainsboro"
          empty-icon="$ratingFull"
          readonly
        ></v-rating>
        <v-card-actions class="justify-space-between">
          <div class="mx-2"></div>
          <router-link to="AllMenus">
          <v-btn class="more" color="secondary" fab x-small dark>
            <v-icon>mdi-arrow-right</v-icon>
          </v-btn>
          </router-link>
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<style>
#RestaurantList {
  text-align: left;
  height: 525px;
}
.more {
  margin-top: -50px;
}
#card {
  margin-top: 20px;
}
a{
  text-decoration: none;
}
</style>

<script>
export default {
  data: () => ({
    Resto: [
      {
        name: "Saga Africa Restaurant",
        address: "Akwa Douala, Cameroon",
        rating: 3,
        coverImage:
          "https://media-cdn.tripadvisor.com/media/photo-s/11/47/90/14/cadre-chaleureux.jpg"
      },
      {
        name: "Mahima Restaurant",
        address: "Douala, Cameroon",
        rating: 2,
        coverImage:
          "https://media-cdn.tripadvisor.com/media/photo-s/04/a0/eb/e6/le-bar.jpg"
      },
      {
        name: "Chateau de Coree - Korean Restaurant",
        address: "Douala Centre, Cameroon",
        rating: 2,
        coverImage: "https://kathalog.net/admin/images/3672062650000.JPG"
      },
      {
        name: "La Fourchette",
        address: "Bamenda Downtown, Cameroon.",
        rating: 2,
        coverImage:
          "https://media-cdn.tripadvisor.com/media/photo-s/16/9c/a4/f3/lynk-prive-the-exclusive.jpg"
      },
      {
        name: "Restaurant A La Broche",
        address: "Bertua, Cameroon",
        rating: 5,
        coverImage:
          "http://www.visiterlafrique.com/wp-content/uploads/2016/12/Visiterlafrique.com-Douala-RegalExpress.jpeg"
      },
      {
        name: "Le C, Douala",
        address: "Buea, Cameroon.",
        rating: 1,
        coverImage: "https://kathalog.net/admin/images/1193922626IMG_5304.JPG"
      }
    ]
  }),
  methods: {
    menusList() {
      //add code that you wish to happen on click
      alert("You requestered to get the menu!");
    }
  }
};
</script>