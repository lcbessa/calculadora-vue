<template>
  <div class="calculator">
    <ComponenteDisplay :value="value" />
    <ComponenteButton label="AC" triple @onCalcButtonClick="clearMemory" />
    <ComponenteButton label="/" operation @onCalcButtonClick="setOperation" />
    <ComponenteButton label="7" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="8" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="9" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="*" operation @onCalcButtonClick="setOperation" />
    <ComponenteButton label="4" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="5" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="6" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="+" operation @onCalcButtonClick="setOperation" />
    <ComponenteButton label="1" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="2" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="3" @onCalcButtonClick="addDigit" />
    <ComponenteButton label="-" operation @onCalcButtonClick="setOperation" />
    <ComponenteButton label="0" double @onCalcButtonClick="addDigit" />
    <ComponenteButton label="." @onCalcButtonClick="addDigit" />
    <ComponenteButton label="=" operation @onCalcButtonClick="setOperation" />
  </div>
</template>

<script>
import ComponenteDisplay from "../components/ComponenteDisplay.vue";
import ComponenteButton from "../components/ComponenteButton.vue";
export default {
  components: {
    ComponenteDisplay,
    ComponenteButton,
  },
  methods: {
    clearMemory() {
      console.log("Limpar Memória");
    },
    setOperation(operation) {
      console.log("Operação" + operation);
    },
    addDigit(n) {
      console.log("Dígito" + n);
    },
  },
};
</script>

<style>
.calculator {
  height: 320px;
  width: 235px;
  border-radius: 5px;

  display: grid;
  grid-template-columns: repeat(4, 25%);
  grid-template-rows: 1fr 48px 48px 48px 48px 48px;
}
</style>