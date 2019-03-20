<template>        
    <b-row v-for="value in item">
        <b-col>{{rt.name}}</b-col>
        <b-col>{{rt.descr}}</b-col>
        <b-col>
            <router-link :to="{ name: 'randomTable', params: { id: rt.id }}">Go to table</router-link>
        </b-col>
    </b-row>
</template>

<script>
export default {
  name: 'random-tables',
  props: {
      item: Object
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
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
