<template>
  <v-app>
 <!-- <v-toolbar app>

    </v-toolbar> -->
      <div class="d-flex align-center">         
      </div>

    <v-main>
      <ourMessages/>
    </v-main>
  </v-app>
</template>

<script>
import ourMessages from './components/ourMessages';

export default {
  name: 'App',

  components: {
    ourMessages,
  },

  data: () => ({
    //
  }),
};
</script>
