<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @btn-click="$emit('toggle-addtask')" :text="this.showAddTask ? 'Close' : 'Add Task'" :color="this.showAddTask ? 'red' : 'green'"/>
  </header>
</template>

<script>
import Button from "./Button";

export default {
  name: "Header",
  props: {
    title: String,
    showAddTask: Boolean,
  },
  components: {Button},
  emits: ['toggle-addtask']
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
