<template>
  <div class="temp">
    <p>Sexe :</p>
    <div class="inline margin-t">
      <input type="radio" id="masculin" name="sexe" value="masculin"  />
      <label for="masculin">Masculin</label>
    </div>
    <div class="inline margin-t margin-b">
      <input type="radio" id="feminin" name="sexe" value="feminin"  />
      <label for="feminin">Féminin</label>
    </div>
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