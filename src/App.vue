<script setup lang="ts">

//no tsc error
import { computeLabel } from "@jsonforms/core";

//throws tsc error
//import { computeLabel } from "@jsonforms/core/src/util/renderer";
</script>

<template>
  {{ computeLabel("name", true, true) }}
</template>

