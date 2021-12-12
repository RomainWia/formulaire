<template>
  <div class="temp">
    <div v-for="item in items" :key="item.name" class="tt" > <!-- ici je créé ma boucle pour avoir tout mes inputs avec les données de mes items -->
        <p class="" >{{item.name}}</p>
        <button class="margin-b button-67 margin-t o" v-on:click.prevent="$emit('addcart')">add to cart</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ScheduleInput",
  props: {
    msg: String,
  },

  data() {
    return {
      items: [
          {name: 'pain'},
          {name: 'poulet'},
          {name: 'tomate'},
          {name: 'eau'},
          {name: 'cable'},
          {name: 'courgette'},
          {name: 'mandarine'},
          {name: 'date'},
          {name: 'banane'},
          {name: 'pomme'}
      ],
    }
  },
  
};
</script>

<style>

</style>