<template>
  <div class="calculator">
    <ComponenteDisplay />
    <ComponenteButton />
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