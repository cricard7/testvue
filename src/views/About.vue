<template>
  <div class="about container bootstrapiso">
    <h1>This is an about page</h1>

      <p>Max's youtube tutorial can be found here <a href="https://www.youtube.com/watch?v=nSmMkeNjjPg" target="_blank">Video</a></p>

<p>Loading sass into our project</p>
<p>to support sass and to be able to install css globally in our project load the following</p>
<p> <code>npm install --save-dev node-sass sass-loader</code></p>
<p>In the root of the project create vue.config.js</p>
<p>configure per <a href="https://vueschool.io/articles/vuejs-tutorials/globally-load-sass-into-your-vue-js-applications/" target="_blank">https://vueschool.io/articles/vuejs-tutorials/globally-load-sass-into-your-vue-js-applications/</a></p>
     
<p>Note that this appears to work if added to App.vue to load a file from node_modules <code>@import "~bootswatch/dist/materia/bootstrap.min.css";</code></p>
<div>
  <p>Or one of the following</p>
<code>
  <ul>
<li>@import "~bootswatch/dist/materia/bootstrap.min.css";</li>
<li>@import "https://stackpath.bootstrapcdn.com/bootswatch/4.1.3/sketchy/bootstrap.min.css";</li>
<li>@import "./assets/sketchy.min.css";</li>
  </ul>
</code>

<p>To create a build that runs using the file protocol set the base URL: https://cli.vuejs.org/config/ </p>
</div>



      <a class="btn btn-primary"> test </a>

<div class="container">
  <div class="jumbotron">
  <h1>Hello</h1>
  </div>
</div>

<h1>A text editor with vue editor</h1>
 <vue-editor v-model="content"></vue-editor>

  <div>
    <h1>The content</h1>
    <span v-html="content"></span>
    <h1>The html</h1>
    {{content}}
  </div>

  </div>
</template>

<script>
import { VueEditor } from "vue2-editor";

export default {
  components: {
    VueEditor
  },

  data() {
    return {
      content: "<h1>Some initial content</h1>"
    };
  }
};
</script>
