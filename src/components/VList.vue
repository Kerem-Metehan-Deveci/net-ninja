<template>
    <ul class="list">
        <v-list-item v-for="item in items" :key="item" :item="item"/>
    </ul>
</template>

<script>
import VListItem from "@/components/VListItem.vue";

  export  default {
    name: 'VList',
    components: {
        VListItem,
    },
    props: {
      items: {
        type: Array,
        default: () => []
      }
    }
  }
</script>