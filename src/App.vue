<template>
  <v-app>
      <fade-transition origin="center" mode="out-in" :duration="250">
        <component :is="layout"></component>
      </fade-transition>
  </v-app>
</template>

<script>
import { mapGetters } from 'vuex';
import { FadeTransition } from "vue2-transitions";

export default {
  name: 'App',
  computed: {
    ...mapGetters(['layout']),
  },
  components: {
    FadeTransition
  },
};
</script>

