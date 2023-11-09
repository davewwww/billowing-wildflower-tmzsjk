<script setup lang="ts">
import { JsonForms } from "@jsonforms/vue";
import { vanillaRenderers } from "@jsonforms/vue-vanilla";
import { useMemory } from "@vueuse/core";

defineProps<{ msg: string }>();

const jsonFormsRenderers = Object.freeze(vanillaRenderers);
const schema = { type: "object", properties: { name: { type: "string" } } };

const { isSupported, memory } = useMemory();
</script>

<template>
  <h1>{{ msg }}</h1>

  <p>{{ isSupported }}, {{ memory }}</p>

  <JsonForms :renderers="jsonFormsRenderers" :schema="schema" :data="{}" />
</template>
