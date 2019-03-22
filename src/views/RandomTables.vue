<template>
  <div class="home">
      <h1>Random Tables</h1>
      <!-- <Header title="Random Titles"/> -->
    <RandomTables :id="$route.params.id"/>
  </div>
</template>

<script>
// @ is an alias to /src
import RandomTables from '@/components/tables/RandomTables.vue'

export default {
  name: 'randomTables',
  components: {
    RandomTables
    }
}
</script>
