<template>
        <b-container>
            <b-row v-for="rt in randomTables">
                <b-col>{{rt.name}}</b-col>
                <b-col>{{rt.descr}}</b-col>
                <b-col>
                    <router-link :to="{ name: 'randomTable', params: { id: rt.id }}">Go to table</router-link>
                </b-col>
            </b-row>
        </b-container>
        
</template>

<script>
export default {
  name: 'random-tables',
  data: function (){
      return {
          randomTables: [
              {
                  id: 1,
                  name: "Common Magic Items",
                  descr: "For Characters Level 1-4"
              },
              {
                  id: 2,
                  name: "Uncommon Magic Items",
                  descr: "For Characters Level 5-9"
              }
          ]
      }
  },
  props: {
      id: Number
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
