<template>
  <div>
    <reorderable-list :items="['A', 'B', 'C']"/>
  </div>
</template>

<script>
import reorderableList from './components/reorderable.vue';

export default {
  name: 'App',
  components: {
    reorderableList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
