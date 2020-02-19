<template>
  <v-app>
    <app-header
      :title="$static.metadata.siteName"
      :items="menuItems"
    />
    <v-content>
      <slot />
    </v-content>
    <app-footer :title="$static.metadata.siteName" />
  </v-app>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import AppHeader from '@/components/layout/AppHeader';
import AppFooter from '@/components/layout/AppFooter';
import menuItems from '@/components/layout/menuItems';

export default {
  components: {
    AppHeader,
    AppFooter,
  },
  data() {
    return {
      menuItems: [...menuItems],
    };
  },
};
</script>
