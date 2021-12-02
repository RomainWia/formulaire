<template>
  <div class="temp">
    <label for="message">Message : </label> <br>
    <textarea name="message" id="message" cols="30" rows="10" placeholder="Taper votre message ici..." class="pdr margin-t margin-b"></textarea>
  </div>
</template>

<script>
export default {
  name: "TextInput",
  props: {
    msg: String,
  },
};
</script>

<style>
</style>