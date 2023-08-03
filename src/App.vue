<script setup>
import eventModifiers from "./components/eventModifiers.vue";
import methods from "./components/methods.vue";
import event2 from "./components/event2.vue";
import conditionalDirectice from "./components/conditionalDirectice.vue";
import listRendering from "./components/listRendering.vue";
import vForObj from "./components/v-for-obj.vue";
import greetingButton from "./components/greetingButton.vue";
import arrayEvenNumbers from "./components/arrayEvenNumbers.vue";
import watchers from "./components/watchers.vue";
import bindingClasses from "./components/bindingClasses.vue";
import listKeys from "./components/list-keys.vue";
</script>

<template>
  <listKeys/>
  <bindingClasses/>
  <watchers></watchers>
  <arrayEvenNumbers></arrayEvenNumbers>
  <greetingButton></greetingButton>
  <listRendering></listRendering>
  <eventModifiers></eventModifiers>
  <methods></methods>
  <event2></event2>
  <conditionalDirectice></conditionalDirectice>
  <vForObj></vForObj>

</template>
