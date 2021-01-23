<template>
  <v-app>
    <v-content>
      <v-container fluid pt-0>
        <router-view />
      </v-container>
    </v-content>
    <Footer>
      <!-- スロットのテスト -->
      <!-- <template #foo="{ items }">{{ items[0].title }}</template>
      <template #bar="{ title, methodName }">
        {{ title }} - {{ methodName }}
      </template> -->
    </Footer>
  </v-app>
</template>

<script>
import { defineComponent } from '@vue/composition-api';
import FooterComponent from '@/components/Footer.vue';

export default defineComponent({
  components: {
    Footer: FooterComponent,
  },
});
</script>
