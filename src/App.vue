<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>The Hack</span>
        <span class="font-weight-light"> 2019</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        href="https://github.com/himself65/hackint-frontend"
        target="_blank"
      >
        <span class="mr-2">GitHub</span>
      </v-btn>
      <v-btn to="about" icon>
        <v-icon>info</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content>
      <RouterView/>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App'
}
</script>
