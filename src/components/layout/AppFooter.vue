<template>
  <v-footer>
    <span>{{ title }}</span>
    <v-spacer />
  </v-footer>
</template>

<script>
export default {
  name: 'AppFooter',
  props: {
    title: {
      type: String,
      default: '',
    },
  },
};
</script>
