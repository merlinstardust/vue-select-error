<script setup lang="ts">
import VueSelect from 'vue-select';
import WelcomeItem from './WelcomeItem.vue';
import DocumentationIcon from './icons/IconDocumentation.vue';
const items = ['C5', 'C6', 'C7', 'C8'];
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Documentation</template>

    Vue’s
    <a href="https://vuejs.org/" target="_blank" rel="noopener">official documentation</a>
    provides you with all information you need to get started.
  </WelcomeItem>
  

  <VueSelect class="custom-styles" :options="items" :value="'C7'" />

</template>

<style>
.custom-styles.v-select {
  width: 100%;
  background-color: white;
}

.custom-styles.v-select .vs__selected,
.custom-styles.v-select .vs__dropdown-option {
  font-size: 30px !important;
}

.custom-styles.v-select .vs__clear {
  padding: 10px;
  margin: -10px 15px -10px 0;
  transform: scale(2);
}
</style>
