<template>
  <div class="temp margin-t margin-b">
    <label for="profession">Profession : </label>
      <select v-model="selected">
        <option v-for="option in options" v-bind:key="option.text" >
          {{option.text}}
        </option>
      </select>
  </div>
  
</template>

<script>
export default {
  name: "MenuSelect",
  props: {
    msg: String,
  },
  data(){
    return {
    selected : 'A',
    options: [
      {text:'Etudiant', value: 'A', colorie:'yellow'},
      {text:'Employé', value:'B', colorie: 'blue'},
      {text:'Freelance', value:'C', colorie:'purple'},
      {text:'Autre', value:'D', colorie:'black'},
    ]
  }
}
};
</script>

<style>
</style>