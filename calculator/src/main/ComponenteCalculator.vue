<template>
  <div class="calculator">
    <ComponenteDisplay value="1000"/>
    <ComponenteButton label="AC" triple />
    <ComponenteButton label="/" operation />
    <ComponenteButton label="7" />
    <ComponenteButton label="8" />
    <ComponenteButton label="9" />
    <ComponenteButton label="*" operation />
    <ComponenteButton label="4" />
    <ComponenteButton label="5" />
    <ComponenteButton label="6" />
    <ComponenteButton label="+" operation />
    <ComponenteButton label="1" />
    <ComponenteButton label="2" />
    <ComponenteButton label="3" />
    <ComponenteButton label="-" operation />
    <ComponenteButton label="0" double />
    <ComponenteButton label="." />
    <ComponenteButton label="=" operation />
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