<template>
  <v-app>
    <v-app-bar app color="yellow" dark>
      <div class="d-flex align-center text-h3 text-center" style="color:black;">
DOCTOR'S NOTE MODULE
      </div>

      <v-spacer></v-spacer>

    </v-app-bar>

    <v-main>
      <OpenDialog />

<DisplayNote></DisplayNote>
      
    </v-main>
  </v-app>
</template>

<style scoped>
@import './main.css';

</style>
<script>

// import TinyMceNote from "./components/TinyMceNote";
import OpenDialog from "./components/OpenDialog.vue";
import DisplayNote from "./components/DisplayNote.vue";

export default {
  name: "App",

  components: {
    // TinyMceNote,
    OpenDialog,
    DisplayNote
},

  data () {
      return {
        dialog: false,
      }
    },
};
</script>
