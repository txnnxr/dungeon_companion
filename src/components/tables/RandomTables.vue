<template>
    <b-container>
        <router-link to="/random-tables" v-if="this.id">Back</router-link>
        <TableHeader v-for="(header, position) in headers" v-bind:header="header" :key="position"/>
        <TableLine v-for="item in tables" v-bind:item="item" :key="item.id" :link="link"/>
    </b-container>
</template>

<script>
import TableHeader from '@/components/tables/TableHeader.vue';
import TableLine from '@/components/tables/TableLine.vue';

export default {
  name: 'random-tables',
  data(){
      return {
          randomTables: []
      };
  },
  beforeMount(){
      //$route = current route
      //$router = vue router instance
    this.getTableData();
  },
  computed: {
    tables(){
        return this.randomTables[this.id];
    },
    headers(){
        return this.tableHeaders[this.id];
    },
    link(){
        return this.id === "";
    } 
  },
  props: {
    id: {
        required: false,
        default: ""
    }  
  },
  methods: {
      getTableData(){
          this.randomTables = {
              "1": [
              {
                  id: 1,
                  name: "+1 Great Axe",
                  descr: "1d8 Slashing Damage"
              },
              {
                  id: 2,
                  name: "+2 Short sword",
                  descr: "1d6 Slashing Damage"
              }
                ],
                "": [
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
          };  
          this.tableHeaders = {
              "1":{
                  1: "Item",
                  2: "Description",
              },
                "": {
                  1: "Table Name",
                  2: "Description",
                  3: "Link"
              },
          };  
      } 
  },
  components:{
      TableLine,
      TableHeader
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
