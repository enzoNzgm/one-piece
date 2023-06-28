<template>
    <v-card
      class="mx-auto"
      max-width="344"
      :color="bg"
    >
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
        cover
      ></v-img>
  
      <v-card-title>
        Top western road trips
      </v-card-title>
  
      <v-card-subtitle>
        1,000 miles of wonder
      </v-card-subtitle>
  
      <v-card-actions>
        <v-btn
          color="orange-lighten-2"
          variant="text"
        >
          Explore
        </v-btn>
  
        <v-spacer></v-spacer>
  
        <v-btn
          :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
          @click="show = !show"
        ></v-btn>
      </v-card-actions>
  
      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>
  
          <v-card-text>
            {{ text.article }}
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
  </template>

<script>
export default {
    name: 'article-one',
    props: {
      bg: String,
      text: String
    },
    data: () => ({
      show: false,
    }),
}
</script>

<style scoped>

</style>