<template>
<div style="width:500px; max-width:500px;">
  <v-container fluid>
    <v-row justify="center">
      <v-col lg="4">
        <v-btn 
          href="https://lnk.to/LAVERS" 
          target="_blank" 
          :ripple="false" 
          :dark="!small" 
          :x-large="!small"
          :small="small" 
          block 
          text 
          class="navButton">
            MUSIC
          </v-btn>
      </v-col>
      <v-col lg="4">
        <v-btn 
          href="https://www.aexattack.com"
          target="_blank" 
          :ripple="false" 
          :dark="!small" 
          :x-large="!small"
          :small="small" 
          block 
          text 
          class="navButton"
        >
          2020
        </v-btn>
      </v-col>
      <v-col lg="4">
        <v-btn 
          href="https://www.instagram.com/axl_aex_vers"
          target="_blank" 
          :ripple="false" 
          :dark="!small" 
          :x-large="!small"
          :small="small" 
          block 
          text 
          class="navButton"
        >CONTACT</v-btn>
      </v-col>
    </v-row>
</v-container>
</div>
</template>
<script>
export default {
  computed: {
    small() {
      if (this.$vuetify.breakpoint.xs || this.$vuetify.breakpoint.s) {
        return true;
      } else {
        return false;
      }
    }
  }
}
</script>
<style scoped>
  .navButton {
    font-family: LetterGothicStd;
    font-weight:bold;
  }
</style>