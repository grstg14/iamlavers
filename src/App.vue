<template>
<div>
  <transition name="fade">
  <v-app 
  v-show="show" 
  :style="{'background-image': 'url(' + bgUrl + ')', 'background-size':'100% auto', 'background-repeat': 'no-repeat'}"
  >

    <v-content>
      <v-container>
        <v-row>
        <v-col lg="4" cols="0" xs="0" s="0"/>

        <v-col lg="4" cols="12" xs="12" s="12">
          <v-row justify="center" :class="marginTop">
            <router-view>
              <Home />
            </router-view>
          </v-row>

          <v-row justify="center"> 
            <navigation />
          </v-row>

          <v-row justify="center">
            <FooterLogos />
          </v-row>
        </v-col>
        <v-col lg="4" cols="0" xs="0" s="0"/>
        </v-row>
      </v-container>
      
    </v-content>

  </v-app>
  </transition>
  </transition>
</div>
</template>

<script>

import Home from '@/views/Home'
import Navigation from '@/components/Navigation'
import FooterLogos from '@/components/Footer'
export default {
  name: 'App',

  components: {
    Home,
    Navigation,
    FooterLogos
  },

  data() {
    return {
      show: false,
      bgBlur: 0
    }
  },

  mounted() {
    this.show = true;
  },


  computed: {
    bgUrl() {
      if ((this.$vuetify.breakpoint.s) || (this.$vuetify.breakpoint.xs)) {
        return "";
      } else {
        return require('@/assets/bg.jpg');
      }
    },

    marginTop() {
      if ((this.$vuetify.breakpoint.s) || (this.$vuetify.breakpoint.xs)) {
        return "mt-2"
      } else {
        return "mt-12"
      }
    }
  },

}
</script>

<style>


.fade-enter {
  filter:sepia(200%);
  filter:blur(100px);
}
.fade-enter-to {
  filter:none;
}
.fade-enter-active, .fade-leave-active {
  transition: all 1.2s;
}

.fade-leave-to {
  filter:sepia(100%);
  filter:(0px);
}


/*.fade-enter, .fade-leave-to  {
filter: none;
}*/
</style>