<template>
  <div class="home">
    <v-textarea
      v-model="kero"
    />
    <v-card>
      <div v-html="aho" />
    </v-card>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'Home',
  data: ()=> ({
    md: require('markdown-it')({
  html: true,
  linkify: true,
  typographer: true
}),
    kero: ""
  }),
  computed: {
    aho: function(){
      return this.md.render(this.kero)
    }
  }
}
</script>
