<template>
  <div> 
    <v-container fluid>
      <v-row justify="center">
        <v-col lg="12">
          <a href="https://www.sissirecords.com/" target="_blank"><v-img max-width="80px" :src="require('@/assets/sr.png')" :class="invertingClass" /></a>
        </v-col>

      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  computed: {
    small() {
      return (this.$vuetify.breakpoint.xs || this.$vuetify.breakpoint.sm || this.$vuetify.breakpoint.md) ? true : false;
    },

    invertingClass() {
      if (!this.small) {
        return "inverted"
      } else {
        return ""
      }
    }
  }
}
</script>

<style scoped>
  .inverted {
    filter: invert(1);
  }
</style>