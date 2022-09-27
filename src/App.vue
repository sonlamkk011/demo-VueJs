<template>
  <div id="app">
    <DemoTasks v-for="(task, index) in tasks" :key="index" :taskData="task" />
    <hr />
    <DemoTag />
    <hr />
    <DemoFormat />
  </div>
</template>

<script>
import DemoTasks from "./components/DemoTasks.vue";
import DemoTag from "./components/DemoTag.vue";
import DemoFormat from "./components/DemoFormat.vue";
export default {
  data() {
    return {
      tasks: [
        { content: "ăn cơm", done: false },
        { content: "code", done: false },
        { content: "nau an", done: false },
        { content: "di ngu", done: false },
      ],
    };
  },
  components: {
    DemoTasks,
    DemoTag,
    DemoFormat
},
};
</script>

<style></style>
