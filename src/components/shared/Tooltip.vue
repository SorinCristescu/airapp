<template>
  <v-tooltip bottom>
    <template>
      <slot></slot>
    </template>
    <span>{{ message }}</span>
  </v-tooltip>
</template>
<script>
export default {
  props: {
    message: {
      type: String,
      required: true,
    },
  },
};
</script>
