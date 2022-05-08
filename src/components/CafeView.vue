<template>
  <div>
    <v-row>
      <v-col>
        <v-breadcrumbs :items="breadcrumbs__items" class="pl-0"></v-breadcrumbs>
      </v-col>
    </v-row>
    <v-row>
      <v-col md="5">
        <v-card>
          <v-img
            height="350"
            src="https://almaty.ppz.kz/upload/iblock/3e9/3e92ff286a1c5e58aa068266edeabe5d.jpg"
            class="d-flex align-end"
          >
            <v-card-title>
              <h2 class="text-h2 white--text">Pinta Bar</h2>
            </v-card-title>
          </v-img>
        </v-card>
      </v-col>
      <v-col md="7">
        <v-card class="h-100">
          <v-card-text>
            <h5 class="text-h5 mb-4">
              Come here if you wanna to taste cool Alcohol
            </h5>

            <v-divider></v-divider>

            <p class="mt-4 text-body-1 mr-5">
              lorem ipsum dolor sit amet, con lorem ipsum dolor sit amet lorem,
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius
              veniam asperiores tenetur in, quae dolorem aliquam libero sit
              similique odit atque doloribus quos repellat quasi ad a. Deleniti,
              molestias odio! Lorem ipsum dolor sit amet consectetur adipisicing
              elit. Dolore cupiditate, in earum reprehenderit perferendis et
              corporis nam quia deleniti! Ipsa neque, itaque animi nisi
              temporibus iusto enim consequatur aut odit. Lorem ipsum dolor sit
              amet, consectetur adipisicing elit. Officiis similique suscipit
              libero velit ducimus, exercitationem, repellat veritatis
              recusandae natus sapiente tempora? Explicabo quos tempora
              excepturi culpa repellat, sint cumque praesentium?
            </p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row class="cafe__menu">
      <v-col md="6">
        <v-card>
          <v-img
            height="450"
            position="center bottom"
            src="https://gdepoest.kz/images/9429940001591975/org/51515121_397426621069428_3958233079592258401_n.jpg"
            class="flex align-end"
          >
          </v-img>
        </v-card>
      </v-col>

      <v-col md="6">
        <v-card>
          <v-card-text>
            <v-list-item-group>
              <v-list-item v-for="item in menu__items" :key="item.id">
                <v-list-item-avatar>
                  <v-img :src="item.img"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                  <v-list-item-title class="text-subtitle-1">
                    {{ item.title }}
                  </v-list-item-title>

                  <v-list-item-subtitle class="text-body-1">
                    {{ item.price }} тг
                  </v-list-item-subtitle>
                </v-list-item-content>

                <v-list-item-action>
                  <v-btn icon>
                    <v-icon color="grey lighten-1">mdi-plus</v-icon>
                  </v-btn>
                </v-list-item-action>
              </v-list-item>
            </v-list-item-group>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <CafeComment></CafeComment>
  </div>
</template>

<script>
import CafeComment from "./CafeComment.vue";

export default {
  name: "CafeView",
  components: {
    CafeComment,
  },
  data: () => ({
    breadcrumbs__items: [
      {
        text: "Home",
        disabled: false,
        href: "/",
      },
      {
        text: "Pinta Bar",
        disabled: true,
        href: "/cafe/view",
      },
    ],
    menu__items: [
      {
        id: 0,
        title: "BBQ Chickens",
        img: "https://izhlife.ru/uploads/posts/2017-04/1493374624_pinta2_compressed.jpg",
        price: 4990,
      },
      {
        id: 1,
        title: "Hamburgers",
        img: "https://pos.zenge.kz/assets/menu/146/1551079455_2bec:800.jpg",
        price: 2500,
      },
      {
        id: 2,
        title: "Shrimps",
        img: "https://pos.zenge.kz/assets/menu/375/1551070450_a3a6:800.jpg",
        price: 5990,
      },
      {
        id: 3,
        title: "Set for beer",
        img: "https://pos.zenge.kz/assets/menu/375/1551070450_a3a6:800.jpg",
        price: 9990,
      },
    ],
  }),
};
</script>

<style></style>
