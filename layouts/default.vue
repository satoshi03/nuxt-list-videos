<template>
  <v-app>
    <v-toolbar
      color="white"
      fixed
      app
    >
      <v-toolbar-title v-text="title"/>
      <v-spacer></v-spacer>
      <v-autocomplete
        v-model="model"
        items="items"
        color="white"
        hide-no-data
        hide-selected
        item-text="Description"
        item-value="API"
        placeholder="検索ワードを入力"
        prepend-icon="mdi-database-search"
        class="mx-3"
        flat
        return-object
      ></v-autocomplete>
      <v-icon>search</v-icon>
    </v-toolbar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; susuru ラーメン検索 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        fixed: false,
        title: 'susuru ラーメン検索'
      }
    }
  }
</script>
