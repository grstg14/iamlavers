<template>
  <div :style="{'max-width': maxWidthImg }">
    <center>
    <v-img id="" max-width="100%" :src="require('@/assets/artwork.jpg')" /></center>
  </div>
</template>

<script>
// @ is an alias to /src
import Naviation from '@/components/Navigation.vue'

export default {
  name: 'Home',
  components: {
    Naviation
  },

  
  computed: {
    maxWidthImg() {
      if ((this.$vuetify.breakpoint.xs) || (this.$vuetify.breakpoint.s)) {
        return "80%"
      } else {
        return "500px"
      }
    }
  }
}
</script>
<style scoped>


#artwork {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.scale-enter {
  width:0%;
}

.scale-enter-to {
  width:100%;
}

.scale-enter-active {
  transition: all 1s;
}
</style>