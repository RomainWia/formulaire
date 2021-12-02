<template>
  <div class="temp margin-b">
    <label for="nom">Nom : </label>
    <input type="text" name="nom" id="nom" class="pdr" required />
  </div>
  <div class="temp margin-b">
    <label for="prenom">Prénom : </label>
    <input type="text" name="prenom" id="prenom" class="pdr" required />
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
