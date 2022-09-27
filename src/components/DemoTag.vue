<template>
  <div class="demo-tag">
    <div class="list">
      <h1>Css selected:</h1>
    <div v-for="(language, index) in languages" 
    :key="index"
    @click=" language.selected = !  language.selected"
    :class="{selected: language.selected}"
    
    >
    <span> {{ language.name }} </span>

    </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      languages: [
       {name:"React Js", selected:false},
       {name:"Node Js", selected:false},
       {name:"Vue Js", selected:false},
       {name:"Three Js", selected:false},
       

      ],
    };
  },
};
</script>

<style scoped>
.list div {
  display: inline;
  border: 3px solid #ebebeb;
  padding: 4px 15px;
  margin-right: 10px;
  border-radius: 15px;
}
.list div.selected{
    background-color: aqua;
    color: black;

}
</style>
