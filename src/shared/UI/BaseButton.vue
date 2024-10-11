<script setup>
defineProps({
  color: {
    type: String,
    default: 'white'
  }
})
</script>

<template>
  <div class="button-wrapper">
    <button class="button">
      {{ $t('tg') }}
      <img src="@/assets/icons/tg.svg" alt="Telegram">
    </button>

    <span class="border" :style="{ borderColor: color }"/>
  </div>
</template>

<style scoped>
button {
  border: none;
  outline: none;
  cursor: pointer;
}

.button-wrapper {
  position: relative;
  width: fit-content;
  max-width: 500px;
}

.button {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  border-radius: 8px;
  padding: 19px 16px;
  color: var(--white);
  background-color: var(--blue);
  font-size: 18px;
  line-height: 24px;
  font-weight: 700;
  position: relative;
  z-index: 2;
}

.border {
  content: '';
  position: absolute;
  top: 6px;
  left: 12px;
  right: -10px;
  bottom: -10px;
  border-radius: 8px;
  border: 2px solid;
  pointer-events: none;
  z-index: 1;
}

@media screen and (max-width: 768px) {
  .button {
    font-size: 12px;
    padding: 10px;
  }

  .button img {
    width: 14px;
    height: 14px;
  }
}
</style>