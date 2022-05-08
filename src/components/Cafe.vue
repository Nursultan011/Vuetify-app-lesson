<template>
  <v-row>
    <v-col class="cafe__component pb-12">
      <h1 class="py-4">Lists of cafes</h1>

      <v-row class="cafe__list">
        <v-col md="4" v-for="cafe in cafes" :key="cafe.id">
          <v-card class="cafe__card">
            <v-img height="250" :src="cafe.image"></v-img>
            <v-card-title>
              <router-link
                to="/cafe/view"
                class="black--text text-decoration-none"
              >
                {{ cafe.name }}
              </router-link>
            </v-card-title>
            <v-card-text>
              <p>{{ cafe.description }}</p>
              <b>Rataing: {{ cafe.rating }} of 5</b>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "Cafe",

  data: () => ({
    cafes: [
      {
        id: "0",
        name: "K-FOOD",
        description: "Here we can cook nice korean food",
        image:
          "https://cdn.vox-cdn.com/thumbor/ebLyPNyZghyiG1TCxQJ5vI-qxvU=/0x0:1280x853/1200x900/filters:focal(538x325:742x529)/cdn.vox-cdn.com/uploads/chorus_image/image/69482129/Aerial_Image__1_.0.jpg",
        tags: ["asian"],
        rating: 3.9,
      },
      {
        id: "1",
        name: "Pinta Bar",
        description: "Here we Pinta bar, nice pivo",
        image:
          "https://almaty.ppz.kz/upload/iblock/3e9/3e92ff286a1c5e58aa068266edeabe5d.jpg",
        tags: ["europe"],
        rating: 4.7,
      },
      {
        id: "2",
        name: "Bahandi",
        description: "Here we can cook nice fastfood Burger",
        image:
          "https://avatars.mds.yandex.net/get-altay/2804357/2a000001704f832982b4ef3636fbd65118b1/XXXL",
        tags: ["american"],
        rating: 4.4,
      },
      {
        id: "3",
        name: "Coffee Boom",
        description: "Here we can cook nice desert and coffee",
        image:
          "https://restolife.kz/upload/information_system_6/2/2/6/item_22625/information_items_property_26352.jpg",
        tags: ["europe"],
        rating: 5,
      },
      {
        id: "4",
        name: "Landzhou",
        description: "Here we can cook nice korean fastfood",
        image:
          "https://imageproxy.wolt.com/venue/5f181527636388afab240dc7/9c703b68-cce1-11ea-af8f-f6042d7101cd_dsc_6996.jpg",
        tags: ["chinese"],
        rating: 4,
      },
      {
        id: "5",
        name: "Del Papa",
        description: "Here we can cook nice italin pasta",
        image:
          "https://weproject.media/upload/iblock/852/852cc75eeb88f49b0ce073f7515d79b1.jpg",
        tags: ["italian"],
        rating: 4.9,
      },
    ],
  }),
};
</script>
