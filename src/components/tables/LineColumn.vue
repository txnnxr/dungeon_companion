<template lang="html">
  <b-col v-if="id != 'id'">{{value}}</b-col>
</template>

<script>
export default {
    name: "LineColumn",
    props: {
        value: {
            required: true
        },
        id:{
            required: true
        }
    }
    
}
</script>
