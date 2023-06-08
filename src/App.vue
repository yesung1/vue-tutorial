@@ -0,0 +1,25 @@
<!--
An example of creating a reusable grid component and using it with external data.
-->

<script setup>
import DemoGrid from './components/Grid.vue'
import { ref } from 'vue'

const searchQuery = ref('')
const gridColumns = ['name', 'power']
const gridData = [
  { name: 'bysuco', power: Infinity },
  { name: 'break', power: 9000 },
  { name: 'cread', power: 7000 },
  { name: 'jomalon', power: 8000 }
]
</script>

<template>
  <form id="search">
    Search <input name="query" v-model="searchQuery">
  </form>
  <DemoGrid :data="gridData" :columns="gridColumns" :filter-key="searchQuery">
  </DemoGrid>
</template>