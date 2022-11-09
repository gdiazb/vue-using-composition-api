<template>
  <li class="list__tweewp">
    <h3 class="tweewp__title">{{ tweepTitle }}</h3>
    <p class="tweewp__description">{{ tweepDescription }}</p>
  </li>
</template>

<script setup>
import { defineProps, toRefs } from "vue";

const props = defineProps({
  tweepTitle: String,
  tweepDescription: String,
});

const { tweepTitle, tweepDescription } = toRefs(props);

</script>
