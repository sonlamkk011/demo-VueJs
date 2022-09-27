<template>
        <div class="demo-task">
        <div>
            <span>{{ taskData.content }}</span>
        </div>
    </div>
   </template>
   
   <script>
   export default {
    props: {
        taskData: Object
    },
    data() {
        return{
            content:"",
        }
    }
   
     
   }
   </script>
   
   <style scoped>
   
   </style>
   