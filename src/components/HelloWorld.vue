<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0);

import { onMounted } from "vue";
// OR use these if you are on Vue 3
import {
  fetchOneEntry,
  RenderContent,
  isPreviewing,
} from "@builder.io/sdk-vue/vue3";
import "@builder.io/sdk-vue/vue3/css";

const canShowContent = ref(false);
const content = ref(null);

onMounted(() => {
  fetchOneEntry({
    model: "page",
    apiKey: "057741175755416385a1000c5f69003a", // Replace with your own API key
    userAttributes: {
      urlPath: window.location.pathname,
    },
  }).then((res) => {
    content.value = res;
    canShowContent.value = content.value || isPreviewing();
  });
});
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>T__________________T</p>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/vuejs/language-tools" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>

  <div>
      <RenderContent
        v-if="canShowContent"
        model="page"
        :content="content"
        :api-key="apiKey"
      />
    </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
