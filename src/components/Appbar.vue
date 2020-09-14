<template>
  <v-app>
    <div>
      <v-app-bar color="deep-purple" dark>
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

        <v-toolbar-title>Restaurant app</v-toolbar-title>
        <v-spacer></v-spacer>

        <v-btn icon v-bind="attrs" v-on="on">
          <v-badge :content="1" :value="1" color="primary" transition>
            <v-icon>mdi-basket</v-icon>
          </v-badge>
        </v-btn>

        <v-menu left bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn icon v-bind="attrs" v-on="on">
              <v-icon>mdi-account-circle</v-icon>
            </v-btn>
          </template>

          <v-list>
            <v-list-item @click="() => {}">
              <v-list-item-title>Login</v-list-item-title>
            </v-list-item>

            <v-list-item @click="() => {}">
              <v-list-item-title>Account</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </v-app-bar>
      <router-view />
      <v-navigation-drawer style="z-index: 10" v-model="drawer" absolute temporary>
        <v-list nav dense>
          <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
            <router-link to="/">
              <v-list-item>
                <v-list-item-icon>
                  <v-icon>mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title>Home</v-list-item-title>
              </v-list-item>
            </router-link>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </div>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: false
  })
};
</script>
