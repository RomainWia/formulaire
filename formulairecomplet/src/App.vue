<template>
<div class="box-s">
  <form action="" method="get" >
    <div v-if="step === 'step 1'">
      <h1 class="margin-b">Etape:1</h1>
      <TextInput msg=""  />
      <DateInput msg=""  />
      <button v-on:click="step='step 2'" class="margin-b button-67 margin-t" >valider</button>
    </div>
    <div v-if="step === 'step 2'">
      <h1>Etape:2</h1>
      <TextArea msg="" />
      <MenuSelect msg="" v-on:couleur="onClickChild"/>
      <button v-on:click="step='step 3'" class="button-67 margin-t">valider</button>
    </div>
    <div v-if="step === 'step 3'">
      <h1>Etape:3</h1>
      <MenuRadio msg="" />
      <input type="submit" value="validation formulaire" class="button-67 margin-t">
    </div>
  </form>
</div>
  
</template>

<script>
import TextInput from "./components/TextInput.vue";
import DateInput from "./components/DateInput.vue";
import TextArea from "./components/TextArea.vue";
import MenuSelect from "./components/MenuSelect.vue";
import MenuRadio from "./components/MenuRadio.vue";


export default {
  name: 'App',
  components: {
    TextInput,
    DateInput,
    TextArea,
    MenuSelect,
    MenuRadio
  },
  data() {
    return {
      colorie: 'red',
      step:'step 1'
    }
  },
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: right;
    color: #2c3e50;
    margin-top: 60px;
    padding-left:30%;
    padding-right:30%;
  }

  .box-s {
    background-color: #F5F5FA;
    border-radius: 30px;
    padding-top: 20px;
    padding-bottom: 20px;
    padding-right: 40px;
  }

  .margin-b {
    margin-bottom: 1em;
  }
  .margin-t {
    margin-top: 1em;
  }
  .pdr {
    padding-right: 80px;
  }

  
  .button-67 {
    margin-right: 0px;
    align-items: center;
    background: #f5f5fa;
    border: 0;
    border-radius: 8px;
    box-shadow: -10px -10px 30px 0 #fff,10px 10px 30px 0 #1d0dca17;
    box-sizing: border-box;
    color: #2a1f62;
    cursor: pointer;
    font-family: "Cascadia Code",Consolas,Monaco,"Andale Mono","Ubuntu Mono",monospace;
    font-size: 1rem;
    justify-content: center;
    line-height: 1.5rem;
    padding: 15px;
    text-align: left;
    transition: .2s;
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
    white-space: pre;
    word-break: normal;
    word-spacing: normal;
  }

  .button-67:hover {
    background: #f8f8ff;
    box-shadow: -15px -15px 30px 0 #fff, 15px 15px 30px 0 #1d0dca17;
  }

  @media (min-width: 768px) {
    .button-67 {
      padding: 24px;
    }
  }

</style>
