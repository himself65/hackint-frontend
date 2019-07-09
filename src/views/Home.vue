<template>
  <v-container>
    <v-layout
      align-center
      justify-center
    >
      <v-layout align-center justify-center>
        <h1 class="grey--text darken-3 group-name display-3 font-weight-thin mb-3">
          自函子范畴上的幺半裙
        </h1>
      </v-layout>
    </v-layout>
    <Members/>
  </v-container>
</template>

<script>
import Members from '../components/Members'

export default {
  name: 'Home',
  components: { Members }
}
</script>

<style lang="stylus" scoped>
  .group-name {
    padding-top 10rem
  }
</style>
