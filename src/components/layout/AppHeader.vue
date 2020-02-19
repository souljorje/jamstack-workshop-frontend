<template>
  <v-app-bar
    app
    dense
  >
    <v-app-bar-nav-icon
      class="hidden-sm-and-up"
      @click.stop="toggleSidebarMenu"
    />
    <g-link
      to="/"
      exact
    >
      <v-toolbar-title>
        {{ title }}
      </v-toolbar-title>
    </g-link>
    <v-spacer />
    <v-toolbar-items class="hidden-xs-only ml-2">
      <v-btn
        v-for="item in items"
        :key="item.title"
        text
        tag="g-link"
        :to="item.to"
        exact
      >
        {{ item.title }}
      </v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
export default {
  name: 'AppHeader',
  props: {
    title: {
      type: String,
      default: '',
    },
    items: {
      type: Array,
      default: () => [],
    },
  },
};
</script>
