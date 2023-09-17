<script setup>
// import $ from "jquery";
import Editor from '@tinymce/tinymce-vue'

</script>
<template>
    <v-card class="h-100">
      <Editor     
        api-key="2mk0bzewgp664s2euusvnclv46w0tshbypq1ljdzn4wj3bkp"
        :init="{
          plugins: 'link image'
        }"
        style="height:100%"
        @init="handleInit"
        @destroy="handleDestroy"
        @change="handleChange"
        @input="handleInput"
        @error="handleError"
        v-model="output"
        :config="config"
        name="qwerty"
        ref="ref"
      />
      <v-card-actions class="justify-end">
        <v-btn
          color="green"
          text-color="white"
          @click="dialog.value = false"
        >Save</v-btn>
      </v-card-actions>
    </v-card>
    
</template>

<script>



const config = {
  height: 600,
  inline: false,
  theme: 'modern',
  fontsize_formats: "8px 10px 12px 14px 16px 18px 20px 22px 24px 26px 28px 30px 34px 38px 42px 48px 54px 60px",
  plugins: 'print preview fullpage powerpaste searchreplace autolink directionality advcode visualblocks visualchars fullscreen image link media template codesample table charmap hr pagebreak nonbreaking anchor toc insertdatetime advlist lists textcolor wordcount tinymcespellchecker a11ychecker imagetools mediaembed  linkchecker contextmenu colorpicker textpattern help',
  toolbar1: 'formatselect fontsizeselect | bold italic strikethrough forecolor backcolor | link | alignleft aligncenter alignright alignjustify  | numlist bullist outdent indent  | removeformat',
  image_advtab: true,
  templates: [
    { title: 'Test template 1', content: 'Test 1' },
    { title: 'Test template 2', content: 'Test 2' }
  ],
  content_css: [
    '//fonts.googleapis.com/css?family=Lato:300,300i,400,400i',
    '//www.tinymce.com/css/codepen.min.css'
  ],
};
export default {
  methods:{
    handleInit (editor) {
      console.log('Initialized');
      console.log(editor)
    },
    
    handleDestroy (editor) {
      console.log('Destroyed');
      console.log(editor)
    },
    
    handleChange (value) {
      console.log('Changed');
      console.log(value)
    },
    
    handleInput (value) {
      console.log('Input');
      console.log(value)
    },
    
    handleError (err) {
      console.log('An error occurred');
      console.log(err)
    }
  },
  data:() => ({
    config,
    output: `<p style="text-align: center;"><span style="font-size: 30px;"><span style="color: #35495e;">
        <span style="color: #1975d1;">HELLO WORLD</span></p>
        `
        })
  }

</script>