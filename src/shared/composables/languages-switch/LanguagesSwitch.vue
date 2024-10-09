<script setup>
import useLanguageSwitch from '@/shared/composables/languages-switch/useLanguageSwitch.js'
import formatCamelCase from '@/shared/utils/formatCamelCase.js'

const {
  currentLanguage,
  changeLanguage,
  languages
} = useLanguageSwitch();
</script>

<template>
  <div class="lang-wrapper" style="">
    <button
      v-for="lang in languages"
      class="language-button"
      :key="lang"
      :class="{ active: currentLanguage === lang }"
      @click="changeLanguage(lang)"
    >
      {{ formatCamelCase(lang) }}
    </button>
  </div>
</template>

<style scoped>
.lang-wrapper {
  display: flex;
  gap: 16px;
  align-items: center;
}

.language-button {
  background: none;
  border: none;
  cursor: pointer;
  color: var(--white);
  font-weight: 500;
  font-size: 18px;
  line-height: 21px;
  text-decoration: none;
}

.language-button.active {
  text-decoration: underline;
  font-weight: 700;
  font-size: 18px;
  line-height: 24px;
}

@media screen and (max-width: 768px) {
  .language-button {
    font-size: 20px;
    line-height: 28px;
  }

  .language-button.active {
    font-size: 20px;
    line-height: 24px;
  }

  .lang-wrapper {
    gap: 30px;
  }
}
</style>
