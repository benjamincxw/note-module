<template>
    <v-row justify="space-around">
        <v-col class="middle-line" >
            <!-- RIGHT SIDE -->
            <div class="text-h3 pa-12 text-center">RIGHT</div>
            <v-list style="max-height: 500px" class="overflow-y-auto">
                <template>
                    <v-card 
                    v-for="item in noteLists" :key="item.message"
                    @click="myClick()"
                    class="mx-auto"
                    max-width="90%">
                        <v-card-text>
                        <p class="text-h4 text--primary">
                            {{item.message}}
                        </p>
                        <p>adjective</p>
                        <div class="text--primary">
                            well meaning and kindly.<br>
                            "a benevolent smile"
                        </div>
                        </v-card-text>
                        <v-card-actions>
                        <v-btn
                            text
                            color="deep-purple accent-4"
                        >
                            EDIT
                        </v-btn>
                        </v-card-actions>
                    </v-card>
                </template>
            </v-list>
        </v-col>
        <!-- LEFT SIDE -->
        <v-col>
            <div class="text-h3 pa-12 text-center">LEFT</div>
            <v-list style="max-height: 500px" class="overflow-y-auto">
                <template>
                    <v-card 
                    v-for="item in noteLists" :key="item.message"
                    @click="myClick()"
                    class="mx-auto"
                    max-width="90%">
                        <v-card-text>
                        <p class="text-h4 text--primary">
                            {{item.message}}
                        </p>
                        <p>adjective</p>
                        <div class="text--primary">
                            well meaning and kindly.<br>
                            "a benevolent smile"
                        </div>
                        </v-card-text>
                        <v-card-actions>
                        <v-btn
                            text
                            color="deep-purple accent-4"
                        >
                            EDIT
                        </v-btn>
                        </v-card-actions>
                    </v-card>
                </template>
            </v-list>
        </v-col>
    </v-row>
</template>
<script>
export default {
  methods:{
    myClick(){
      console.log('I am click')
    }
  },
  data() {
    return {
        noteLists: [
        {message: 'Retina'},
        {message: 'Pupil'},
        {message: 'Cornea'},
        {message: 'Lens'},
        {message: 'Iris'},
        {message: 'Sclera'}
        ]
    }
  }
}
</script>
<style>
.middle-line{
    padding-right:20px;
    border-right: 1px solid #000000;
}
.v-card{
    margin-top: 10px !important;
}
.v-card:focus {
    background-color: rgb(179, 179, 252) !important ;
}
  
.v-card--link:focus::before {
    opacity: 0 !important ;
}

</style>