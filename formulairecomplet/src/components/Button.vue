<template>
    <button class="margin-b button-67 margin-t o" v-on:click.prevent="$emit('colorchangered')">R</button>
    <button class="margin-b button-67 margin-t o" v-on:click.prevent="$emit('colorchangegreen')">G</button>
    <button class="margin-b button-67 margin-t o" v-on:click.prevent="$emit('colorchangeblue')">B</button>
    <button class="margin-b button-67 margin-t o" v-on:click.prevent="$emit('colorchangebasic')">reset</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    msg: String,
  },
};
</script>

<style>
.o {
    margin-left: 10px;
}
</style>