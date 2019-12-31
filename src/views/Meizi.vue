<template>
    <v-row>
      <v-col cols="1" sm="1" md="4" lg="8" xl="12">
        <v-card>
          <v-container fluid>
            <v-row>
              <v-col
                v-for="n in 320"
                :key="n"
                class="d-flex child-flex"
                cols="2"
              >
                <v-card flat tile class="d-flex">
                  <v-img
                    :src="get_img_url(n)"
                    :lazy-src="get_img_url(n)"
                    class="grey lighten-2"
                  >
                    <template v-slot:placeholder>
                      <v-row
                        class="fill-height ma-0"
                        align="center"
                        justify="center"
                      >
                      <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                      </v-row>
                    </template>
                    <div>{{image_lists[n].title}}</div>
                  </v-img>
                </v-card>


              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>
    </v-row>
</template>

<script>
import image_lists_json from "@/assets/image_lists.json";

export default {
  data: () => ({
    image_lists: image_lists_json
  }),
  methods: {
    get_img_url: function (n) {
      //console.log(value)
      return this.image_lists[n].src
    }
  },
}
</script>

<style>

</style>
