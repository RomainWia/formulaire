<template>
  <div class="temp margin-t margin-b">
    <label for="profession">Couleur : </label>
      <select v-model="selected">
        <option v-for="option in options" value="option.colorie" v-bind:key="option.text" >
          {{option.text}}
        </option>
      </select>
  </div>
</template>

<script>
export default {
    name: "CouleurSelect",
    props: {
        msg: String,
    },
    data(){
        return {
            selected : null,
            options: [
            {text:'Jaune', value: 'A', colorie:'yellow'},
            {text:'Bleu', value:'B', colorie: 'blue'},
            {text:'Violet', value:'C', colorie:'purple'},
            {text:'Noir', value:'D', colorie:'black'},
            ]
        }
    },
    methods: {
        changedLabel(event) {
            this.selected = event;
        }
    }
};

</script>

<style >
</style>