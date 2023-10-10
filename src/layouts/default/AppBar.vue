<template>
  <v-card class="navbar">
    <v-tabs v-model="tab" class="navbar-tabs">
      <v-tab class="navbar-tab">
        <router-link :to="{ name: 'Home' }" class="navbar-link">Home</router-link>
      </v-tab>
      <v-tab class="navbar-tab">
        <router-link :to="{ name: 'About' }" class="navbar-link">About Us</router-link>
      </v-tab>
      <v-tab class="navbar-tab">
        <router-link :to="{ name: 'Members' }" class="navbar-link">Members</router-link>
      </v-tab>
      <v-tab class="navbar-tab">
        <router-link :to="{ name: 'Portfolio' }" class="navbar-link">Portfolio</router-link>
      </v-tab>
      <v-tab class="navbar-tab">
        <router-link :to="{ name: 'Contact' }" class="navbar-link">Contact</router-link>
      </v-tab>
    </v-tabs>
    <router-view></router-view>
  </v-card>
</template>

<style scoped>
.navbar {
  background-color: white;
}

.navbar-tabs {
  color: black;
  font-family: 'Lora', serif;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
}

.navbar-tab {
  font-size: 20px;
}

.navbar-link {
  text-decoration: none; /* Elimina la decoración de enlace */
  color: black;
  font-family: 'Lora', serif;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}
</style>

<script>
import { RouterLink } from 'vue-router';

export default {
  components: {
    RouterLink,
  },
  data: () => ({
    tab: null,
  }),
}
</script>
