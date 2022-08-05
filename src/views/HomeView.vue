<template>
  <div class="home m-auto d-flex justify-content-flex-start flex-wrap">
    <v-main>
      <v-container>
        <v-row>
          <v-col v-for="item in items" :key="item" cols="4">
            <v-card>
              <v-img :src="item.img" max-width="300px" height="200px"></v-img>

              <v-card-title>{{ item.title }} </v-card-title>

              <v-card-subtitle> 1,000 miles of views </v-card-subtitle>

              <v-card-actions>
                <v-btn color="orange lighten-2" text> Hot</v-btn>

                <v-spacer></v-spacer>

                <v-btn icon @click="show = !show">
                  <v-icon>{{
                    show ? "mdi-chevron-up" : "mdi-chevron-down"
                  }}</v-icon>
                </v-btn>
              </v-card-actions>

              <v-expand-transition>
                <div v-show="show">
                  <v-divider></v-divider>
                </div>
              </v-expand-transition>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  components: {},
  data: () => ({
    show: false,
    items: [
      {
        img: "https://prod-ripcut-delivery.disney-plus.net/v1/variant/disney/37DB4A66127CD0A07F802DDE9E7D42FC8B1C6864DAD4E48B072AB94AC2A4FF3D/scale?width=1200&aspectRatio=1.78&format=jpeg",
        title: "Spiderman Far from Home",
      },
      { img: "1.jpg", title: "Teacher and little Crocodile" },
      { img: "spider.jpg", title: "PN Marvel Vue War" },
    ],
  }),
};
</script>
