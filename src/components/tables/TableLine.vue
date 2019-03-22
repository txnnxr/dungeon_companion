<template>
    <b-row>
        <LineColumn v-for="(value, id) in item" v-bind:value="value" v-bind:id="id" v-bind:key="id"/>
        <router-link v-if="link" :to="{ name: 'randomTable', params: { id: item.id }}">Go to table</router-link>
    </b-row>
</template>

<script>
import LineColumn from '@/components/tables/LineColumn.vue';

    export default {
        name: 'TableLine',
        props: {
            item: {
                type: Object,
                required: true
            },
            id: {
                type: Number,
                required: false
            },
            link: {
                required: false
            }
        },
        components:{
            LineColumn
        }
    }
</script>
