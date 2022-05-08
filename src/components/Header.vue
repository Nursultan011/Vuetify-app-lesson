<template>
  <div>
    <v-app-bar color="blue" app>
      <v-col class="font-weight-bold white--text d-flex align-center">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-app-bar-title>iFood</v-app-bar-title>
      </v-col>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute left temporary>
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="text--acent-4">
          <v-list-item>
            <v-list-item-title>List of Cafes</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>About</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Contacts</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>

<style></style>
