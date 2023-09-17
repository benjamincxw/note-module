
<template>
    <v-row justify="space-around">
        
        <v-col cols="auto" style="margin:12px">
          <v-dialog
            transition="dialog-top-transition"
            max-width="600"
          >
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                color="yellow"
                v-bind="attrs"
                v-on="on"
              ><span>Create a Note</span></v-btn>
            </template>
            <template v-slot:default="dialog">
              <v-card>
                <v-toolbar
                  color="primary"
                  dark
                >Doc, please write your note here</v-toolbar>
                <v-card-text style="height:600px">
                  <TinyMceNote/>
                </v-card-text>
                <v-card-actions class="justify-end">
                  <v-btn
                  style="display:none"
                    color="green"
                    text-color="white"
                    @click="dialog.value = false"
                  >Save</v-btn>
                </v-card-actions>
              </v-card>
            </template>
          </v-dialog>
        </v-col>
      </v-row>
  </template>

  <script>
    import TinyMceNote from "./TinyMceNote";

  export default {
    data () {
      return {
        dialog: false,
      }
    },
    components: {
    TinyMceNote,
  },
  };

</script>