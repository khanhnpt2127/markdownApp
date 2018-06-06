<template>
  <!-- Notebook app -->
  <div id="notebook">
    <!-- Main pane -->
    <section class="main">
      <textarea v-model="content"></textarea>
      <div v-html="content"> </div>
    </section>
  </div>
</template>

<script>

import * as marked from 'marked'

export default {
  name: "HelloWorld",
  data() {
    const html = marked('**bold** *Italic* [link](www.google.com)')
    console.log(html)


    return {
      content: marked('')
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
