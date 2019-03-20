<template>
  <div class="home">
      <h1>Random Tables</h1>
    <RandomTables />
  </div>
</template>

<script>
// @ is an alias to /src
import RandomTables from '@/components/RandomTables.vue'

export default {
  name: 'randomTables',
  components: {
    RandomTables
  }
}
</script>
