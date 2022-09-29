<template>
  <nav>
    <v-navigation-drawer v-model="drawer" dark app mini-variant mini-variant-width="100" class="light-blue darken-4">
      <v-list>

        <v-list-item class="mb-16">
          <v-list-item-content>
            <v-icon class="mb-2" large color="teal accent-2">fas fa-dove</v-icon>
          </v-list-item-content>
        </v-list-item>

      </v-list>
   
      <v-list style="position: absolute; bottom: 0" class="ml-5" flat>
        <v-list-item router to="/">
          <v-list-item-content>
            <v-icon color="grey">fas fa-users</v-icon>
          </v-list-item-content>
        </v-list-item>
        <v-list-item router to="/">
          <v-list-item-content>
            <v-icon color="grey">fas fa-cog</v-icon>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>
<script>
  export default {
    data: () =>({
      drawer: true
    })
  }
</script>