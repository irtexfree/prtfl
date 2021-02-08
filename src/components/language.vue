<template>
  <div>
    <select v-model="$i18n.locale">
      <option v-for="lang in langs" :key="lang" :value="lang">
        {{ lang }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  name: "SwitchLocale",
  data() {
    return { langs: ["en", "ru"] };
  },
};
</script>