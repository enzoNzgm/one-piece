<template>
     <v-container >
        <v-row no-gutters>
        <v-col
            v-for="(item, i) in items" :key="i"
            cols="12"
            sm="4"
        >
        <Article :bg="item.bg" :text="item" v-if="i >= 2"  />
        <Article :bg="item.bg" :text="item" v-else  />
        </v-col>
        </v-row>
    </v-container>
  </template>
  
  <script>
  import Article from './Articleone.vue';
  
  export default {
    name: 'article-all',
    data: () => ({
      items: [
        { article: "article 1", bg: "#ff7"},
        { article: "article 2", bg: "#f7f"},
        { article: "article 3", bg: "#5f7"},
        { article: "article 4", bg: "#f78"},
        { article: "article 5", bg: "#0f7"},
      ]
    }),
    components: {
      Article
    }
  }
  </script>
  
  <style>
  
  </style>
  